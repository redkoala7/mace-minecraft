
```
        public static int RotateMushroom(int intData, int intRotation)
        {
            switch (intData)
            {
                case (int)HugeMushroomType.STEM:
                case (int)HugeMushroomType.FLESHY:
                case (int)HugeMushroomType.CAP_TOP:
                    return intData;
            }
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)HugeMushroomType.CAP_CORNER_NORTHWEST: return (int)HugeMushroomType.CAP_CORNER_SOUTHWEST;
                        case (int)HugeMushroomType.CAP_CORNER_NORTHEAST: return (int)HugeMushroomType.CAP_CORNER_NORTHWEST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHEAST: return (int)HugeMushroomType.CAP_CORNER_NORTHEAST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHWEST: return (int)HugeMushroomType.CAP_CORNER_SOUTHEAST;
                        case (int)HugeMushroomType.CAP_SIDE_NORTH: return (int)HugeMushroomType.CAP_SIDE_WEST;
                        case (int)HugeMushroomType.CAP_SIDE_EAST: return (int)HugeMushroomType.CAP_SIDE_NORTH;
                        case (int)HugeMushroomType.CAP_SIDE_SOUTH: return (int)HugeMushroomType.CAP_SIDE_EAST;
                        case (int)HugeMushroomType.CAP_SIDE_WEST: return (int)HugeMushroomType.CAP_SIDE_SOUTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)HugeMushroomType.CAP_CORNER_NORTHWEST: return (int)HugeMushroomType.CAP_CORNER_NORTHEAST;
                        case (int)HugeMushroomType.CAP_CORNER_NORTHEAST: return (int)HugeMushroomType.CAP_CORNER_SOUTHEAST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHEAST: return (int)HugeMushroomType.CAP_CORNER_SOUTHWEST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHWEST: return (int)HugeMushroomType.CAP_CORNER_NORTHWEST;
                        case (int)HugeMushroomType.CAP_SIDE_NORTH: return (int)HugeMushroomType.CAP_SIDE_EAST;
                        case (int)HugeMushroomType.CAP_SIDE_EAST: return (int)HugeMushroomType.CAP_SIDE_SOUTH;
                        case (int)HugeMushroomType.CAP_SIDE_SOUTH: return (int)HugeMushroomType.CAP_SIDE_WEST;
                        case (int)HugeMushroomType.CAP_SIDE_WEST: return (int)HugeMushroomType.CAP_SIDE_NORTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)HugeMushroomType.CAP_CORNER_NORTHWEST: return (int)HugeMushroomType.CAP_CORNER_SOUTHEAST;
                        case (int)HugeMushroomType.CAP_CORNER_NORTHEAST: return (int)HugeMushroomType.CAP_CORNER_SOUTHWEST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHEAST: return (int)HugeMushroomType.CAP_CORNER_NORTHWEST;
                        case (int)HugeMushroomType.CAP_CORNER_SOUTHWEST: return (int)HugeMushroomType.CAP_CORNER_NORTHEAST;
                        case (int)HugeMushroomType.CAP_SIDE_NORTH: return (int)HugeMushroomType.CAP_SIDE_SOUTH;
                        case (int)HugeMushroomType.CAP_SIDE_EAST: return (int)HugeMushroomType.CAP_SIDE_WEST;
                        case (int)HugeMushroomType.CAP_SIDE_SOUTH: return (int)HugeMushroomType.CAP_SIDE_NORTH;
                        case (int)HugeMushroomType.CAP_SIDE_WEST: return (int)HugeMushroomType.CAP_SIDE_EAST;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotateTorch(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)TorchOrientation.FLOOR: return (int)TorchOrientation.FLOOR;
                        case (int)TorchOrientation.NORTH: return (int)TorchOrientation.WEST;
                        case (int)TorchOrientation.EAST: return (int)TorchOrientation.NORTH;
                        case (int)TorchOrientation.SOUTH: return (int)TorchOrientation.EAST;
                        case (int)TorchOrientation.WEST: return (int)TorchOrientation.SOUTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)TorchOrientation.FLOOR: return (int)TorchOrientation.FLOOR;
                        case (int)TorchOrientation.NORTH: return (int)TorchOrientation.EAST;
                        case (int)TorchOrientation.EAST: return (int)TorchOrientation.SOUTH;
                        case (int)TorchOrientation.SOUTH: return (int)TorchOrientation.WEST;
                        case (int)TorchOrientation.WEST: return (int)TorchOrientation.NORTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)TorchOrientation.FLOOR: return (int)TorchOrientation.FLOOR;
                        case (int)TorchOrientation.NORTH: return (int)TorchOrientation.SOUTH;
                        case (int)TorchOrientation.EAST: return (int)TorchOrientation.WEST;
                        case (int)TorchOrientation.SOUTH: return (int)TorchOrientation.NORTH;
                        case (int)TorchOrientation.WEST: return (int)TorchOrientation.EAST;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotateLever(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booPowered = false;
                if (intData >= (int)LeverState.POWERED)
                {
                    intData -= (int)LeverState.POWERED;
                    booPowered = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)LeverOrientation.NORTH: intDirection = (int)LeverOrientation.WEST; break;
                            case (int)LeverOrientation.EAST: intDirection = (int)LeverOrientation.NORTH; break;
                            case (int)LeverOrientation.SOUTH: intDirection = (int)LeverOrientation.EAST; break;
                            case (int)LeverOrientation.WEST: intDirection = (int)LeverOrientation.SOUTH; break;
                            case (int)LeverOrientation.GROUND_EASTWEST: intDirection = (int)LeverOrientation.GROUND_NORTHSOUTH; break;
                            case (int)LeverOrientation.GROUND_NORTHSOUTH: intDirection = (int)LeverOrientation.GROUND_EASTWEST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)LeverOrientation.NORTH: intDirection = (int)LeverOrientation.EAST; break;
                            case (int)LeverOrientation.EAST: intDirection = (int)LeverOrientation.SOUTH; break;
                            case (int)LeverOrientation.SOUTH: intDirection = (int)LeverOrientation.WEST; break;
                            case (int)LeverOrientation.WEST: intDirection = (int)LeverOrientation.NORTH; break;
                            case (int)LeverOrientation.GROUND_EASTWEST: intDirection = (int)LeverOrientation.GROUND_NORTHSOUTH; break;
                            case (int)LeverOrientation.GROUND_NORTHSOUTH: intDirection = (int)LeverOrientation.GROUND_EASTWEST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)LeverOrientation.NORTH: intDirection = (int)LeverOrientation.SOUTH; break;
                            case (int)LeverOrientation.EAST: intDirection = (int)LeverOrientation.WEST; break;
                            case (int)LeverOrientation.SOUTH: intDirection = (int)LeverOrientation.NORTH; break;
                            case (int)LeverOrientation.WEST: intDirection = (int)LeverOrientation.EAST; break;
                            case (int)LeverOrientation.GROUND_EASTWEST: intDirection = (int)LeverOrientation.GROUND_EASTWEST; break;
                            case (int)LeverOrientation.GROUND_NORTHSOUTH: intDirection = (int)LeverOrientation.GROUND_NORTHSOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booPowered)
                {
                    intDirection += (int)LeverState.POWERED;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotateWallSignOrLadderOrFurnanceOrDispenser(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)WallSignOrientation.NORTH: return (int)WallSignOrientation.WEST;
                        case (int)WallSignOrientation.EAST: return (int)WallSignOrientation.NORTH;
                        case (int)WallSignOrientation.SOUTH: return (int)WallSignOrientation.EAST;
                        case (int)WallSignOrientation.WEST: return (int)WallSignOrientation.SOUTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)WallSignOrientation.NORTH: return (int)WallSignOrientation.EAST;
                        case (int)WallSignOrientation.EAST: return (int)WallSignOrientation.SOUTH;
                        case (int)WallSignOrientation.SOUTH: return (int)WallSignOrientation.WEST;
                        case (int)WallSignOrientation.WEST: return (int)WallSignOrientation.NORTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)WallSignOrientation.NORTH: return (int)WallSignOrientation.SOUTH;
                        case (int)WallSignOrientation.EAST: return (int)WallSignOrientation.WEST;
                        case (int)WallSignOrientation.SOUTH: return (int)WallSignOrientation.NORTH;
                        case (int)WallSignOrientation.WEST: return (int)WallSignOrientation.EAST;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotatePortal(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1: case 3:
                    return 2;
                default:
                    return intData;
            }
        }
        public static int RotateStairs(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)StairOrientation.ASCEND_NORTH: return (int)StairOrientation.ASCEND_WEST;
                        case (int)StairOrientation.ASCEND_EAST: return (int)StairOrientation.ASCEND_NORTH;
                        case (int)StairOrientation.ASCEND_SOUTH: return (int)StairOrientation.ASCEND_EAST;
                        case (int)StairOrientation.ASCEND_WEST: return (int)StairOrientation.ASCEND_SOUTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)StairOrientation.ASCEND_NORTH: return (int)StairOrientation.ASCEND_EAST;
                        case (int)StairOrientation.ASCEND_EAST: return (int)StairOrientation.ASCEND_SOUTH;
                        case (int)StairOrientation.ASCEND_SOUTH: return (int)StairOrientation.ASCEND_WEST;
                        case (int)StairOrientation.ASCEND_WEST: return (int)StairOrientation.ASCEND_NORTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)StairOrientation.ASCEND_NORTH: return (int)StairOrientation.ASCEND_SOUTH;
                        case (int)StairOrientation.ASCEND_EAST: return (int)StairOrientation.ASCEND_WEST;
                        case (int)StairOrientation.ASCEND_SOUTH: return (int)StairOrientation.ASCEND_NORTH;
                        case (int)StairOrientation.ASCEND_WEST: return (int)StairOrientation.ASCEND_EAST;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotateRedStoneRepeater(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                int intDelay;
                if (intData >= (int)RepeaterDelay.DELAY_4)
                {
                    intDelay = (int)RepeaterDelay.DELAY_4;
                    intData -= intDelay;
                }
                else if (intData >= (int)RepeaterDelay.DELAY_3)
                {
                    intDelay = (int)RepeaterDelay.DELAY_3;
                    intData -= intDelay;
                }
                else if (intData >= (int)RepeaterDelay.DELAY_2)
                {
                    intDelay = (int)RepeaterDelay.DELAY_2;
                    intData -= intDelay;
                }
                else
                {
                    intDelay = (int)RepeaterDelay.DELAY_1;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)RepeaterOriengation.NORTH: intDirection = (int)RepeaterOriengation.WEST; break;
                            case (int)RepeaterOriengation.EAST: intDirection = (int)RepeaterOriengation.NORTH; break;
                            case (int)RepeaterOriengation.SOUTH: intDirection = (int)RepeaterOriengation.EAST; break;
                            case (int)RepeaterOriengation.WEST: intDirection = (int)RepeaterOriengation.SOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)RepeaterOriengation.NORTH: intDirection = (int)RepeaterOriengation.EAST; break;
                            case (int)RepeaterOriengation.EAST: intDirection = (int)RepeaterOriengation.SOUTH; break;
                            case (int)RepeaterOriengation.SOUTH: intDirection = (int)RepeaterOriengation.WEST; break;
                            case (int)RepeaterOriengation.WEST: intDirection = (int)RepeaterOriengation.NORTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)RepeaterOriengation.NORTH: intDirection = (int)RepeaterOriengation.SOUTH; break;
                            case (int)RepeaterOriengation.EAST: intDirection = (int)RepeaterOriengation.WEST; break;
                            case (int)RepeaterOriengation.SOUTH: intDirection = (int)RepeaterOriengation.NORTH; break;
                            case (int)RepeaterOriengation.WEST: intDirection = (int)RepeaterOriengation.EAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                return intDirection + intDelay;
            }
            else
            {
                return intData;
            }
        }
        public static int RotateFenceGate(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booOpen = false;
                if (intData >= (int)FenceGateState.OPEN)
                {
                    intData -= (int)FenceGateState.OPEN;
                    booOpen = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)FenceGateOrientation.NORTH: intDirection = (int)FenceGateOrientation.WEST; break;
                            case (int)FenceGateOrientation.EAST: intDirection = (int)FenceGateOrientation.NORTH; break;
                            case (int)FenceGateOrientation.SOUTH: intDirection = (int)FenceGateOrientation.EAST; break;
                            case (int)FenceGateOrientation.WEST: intDirection = (int)FenceGateOrientation.SOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)FenceGateOrientation.NORTH: intDirection = (int)FenceGateOrientation.EAST; break;
                            case (int)FenceGateOrientation.EAST: intDirection = (int)FenceGateOrientation.SOUTH; break;
                            case (int)FenceGateOrientation.SOUTH: intDirection = (int)FenceGateOrientation.WEST; break;
                            case (int)FenceGateOrientation.WEST: intDirection = (int)FenceGateOrientation.NORTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)FenceGateOrientation.NORTH: intDirection = (int)FenceGateOrientation.SOUTH; break;
                            case (int)FenceGateOrientation.EAST: intDirection = (int)FenceGateOrientation.WEST; break;
                            case (int)FenceGateOrientation.SOUTH: intDirection = (int)FenceGateOrientation.NORTH; break;
                            case (int)FenceGateOrientation.WEST: intDirection = (int)FenceGateOrientation.EAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booOpen)
                {
                    intDirection += (int)FenceGateState.OPEN;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotatePistonBody(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booExtended = false;
                if (intData >= (int)PistonBodyState.EXTENDED)
                {
                    intData -= (int)PistonBodyState.EXTENDED;
                    booExtended = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booExtended)
                {
                    intDirection += (int)PistonBodyState.EXTENDED;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotatePistonExtension(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booSticky = false;
                if (intData >= (int)PistonHeadState.STICKY)
                {
                    intData -= (int)PistonHeadState.STICKY;
                    booSticky = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)PistonOrientation.NORTH: intDirection = (int)PistonOrientation.SOUTH; break;
                            case (int)PistonOrientation.EAST: intDirection = (int)PistonOrientation.WEST; break;
                            case (int)PistonOrientation.SOUTH: intDirection = (int)PistonOrientation.NORTH; break;
                            case (int)PistonOrientation.WEST: intDirection = (int)PistonOrientation.EAST; break;
                            case (int)PistonOrientation.UP: intDirection = (int)PistonOrientation.UP; break;
                            case 0: intDirection = 0; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booSticky)
                {
                    intDirection += (int)PistonHeadState.STICKY;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotateBed(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booHead = false;
                if (intData >= (int)BedState.HEAD)
                {
                    intData -= (int)BedState.HEAD;
                    booHead = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)BedOrientation.NORTH: intDirection = (int)BedOrientation.WEST; break;
                            case (int)BedOrientation.EAST: intDirection = (int)BedOrientation.NORTH; break;
                            case (int)BedOrientation.SOUTH: intDirection = (int)BedOrientation.EAST; break;
                            case (int)BedOrientation.WEST: intDirection = (int)BedOrientation.SOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)BedOrientation.NORTH: intDirection = (int)BedOrientation.EAST; break;
                            case (int)BedOrientation.EAST: intDirection = (int)BedOrientation.SOUTH; break;
                            case (int)BedOrientation.SOUTH: intDirection = (int)BedOrientation.WEST; break;
                            case (int)BedOrientation.WEST: intDirection = (int)BedOrientation.NORTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)BedOrientation.NORTH: intDirection = (int)BedOrientation.SOUTH; break;
                            case (int)BedOrientation.EAST: intDirection = (int)BedOrientation.WEST;   break;
                            case (int)BedOrientation.SOUTH: intDirection = (int)BedOrientation.NORTH; break;
                            case (int)BedOrientation.WEST: intDirection = (int)BedOrientation.EAST;   break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booHead)
                {
                    intDirection += (int)BedState.HEAD;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotateSignPost(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    intData += 12;
                    break;
                case 2:
                    intData += 4;
                    break;
                case 3:
                    intData += 8;
                    break;
                default:
                    Debug.WriteLine("Oh noes!");
                    break;
            }
            return intData % 16;
        }
        public static int RotateButton(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booPushed = false;
                if (intData >= (int)ButtonState.PRESSED)
                {
                    intData -= (int)ButtonState.PRESSED;
                    booPushed = true;
                }
                int intDirection = 0;
                Debug.WriteLine(intRotation);
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)ButtonOrientation.NORTH: intDirection = (int)ButtonOrientation.EAST; break;
                            case (int)ButtonOrientation.EAST: intDirection = (int)ButtonOrientation.SOUTH; break;
                            case (int)ButtonOrientation.SOUTH: intDirection = (int)ButtonOrientation.WEST; break;
                            case (int)ButtonOrientation.WEST: intDirection = (int)ButtonOrientation.NORTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)ButtonOrientation.NORTH: intDirection = (int)ButtonOrientation.WEST; break;
                            case (int)ButtonOrientation.EAST: intDirection = (int)ButtonOrientation.NORTH; break;
                            case (int)ButtonOrientation.SOUTH: intDirection = (int)ButtonOrientation.EAST; break;
                            case (int)ButtonOrientation.WEST: intDirection = (int)ButtonOrientation.SOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)ButtonOrientation.NORTH: intDirection = (int)ButtonOrientation.SOUTH; break;
                            case (int)ButtonOrientation.EAST: intDirection = (int)ButtonOrientation.WEST; break;
                            case (int)ButtonOrientation.SOUTH: intDirection = (int)ButtonOrientation.NORTH; break;
                            case (int)ButtonOrientation.WEST: intDirection = (int)ButtonOrientation.EAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booPushed)
                {
                    intDirection += (int)ButtonState.PRESSED;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static int RotateTrapdoor(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booOpen = false;
                if (intData >= (int)DoorState.SWUNG)
                {
                    intData -= (int)DoorState.SWUNG;
                    booOpen = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)TrapdoorOrientation.NORTH: intDirection = (int)TrapdoorOrientation.WEST; break;
                            case (int)TrapdoorOrientation.EAST: intDirection = (int)TrapdoorOrientation.NORTH; break;
                            case (int)TrapdoorOrientation.SOUTH: intDirection = (int)TrapdoorOrientation.EAST; break;
                            case (int)TrapdoorOrientation.WEST: intDirection = (int)TrapdoorOrientation.SOUTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)TrapdoorOrientation.NORTH: intDirection = (int)TrapdoorOrientation.EAST; break;
                            case (int)TrapdoorOrientation.EAST: intDirection = (int)TrapdoorOrientation.SOUTH; break;
                            case (int)TrapdoorOrientation.SOUTH: intDirection = (int)TrapdoorOrientation.WEST; break;
                            case (int)TrapdoorOrientation.WEST: intDirection = (int)TrapdoorOrientation.NORTH; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)TrapdoorOrientation.NORTH: intDirection = (int)TrapdoorOrientation.SOUTH; break;
                            case (int)TrapdoorOrientation.EAST: intDirection = (int)TrapdoorOrientation.WEST; break;
                            case (int)TrapdoorOrientation.SOUTH: intDirection = (int)TrapdoorOrientation.NORTH; break;
                            case (int)TrapdoorOrientation.WEST: intDirection = (int)TrapdoorOrientation.EAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booOpen)
                {
                    intDirection += (int)FenceGateState.OPEN;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
        public static EntityPainting.DirectionType RotatePortrait(EntityPainting.DirectionType dtData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (dtData)
                    {
                        case EntityPainting.DirectionType.NORTH: return EntityPainting.DirectionType.WEST;
                        case EntityPainting.DirectionType.EAST: return EntityPainting.DirectionType.NORTH;
                        case EntityPainting.DirectionType.SOUTH: return EntityPainting.DirectionType.EAST;
                        case EntityPainting.DirectionType.WEST: return EntityPainting.DirectionType.SOUTH;
                        default: Debug.Fail("Painting rotation"); break;
                    }
                    return dtData;
                case 2:
                    switch (dtData)
                    {
                        case EntityPainting.DirectionType.NORTH: return EntityPainting.DirectionType.EAST;
                        case EntityPainting.DirectionType.EAST: return EntityPainting.DirectionType.SOUTH;
                        case EntityPainting.DirectionType.SOUTH: return EntityPainting.DirectionType.WEST;
                        case EntityPainting.DirectionType.WEST: return EntityPainting.DirectionType.NORTH;
                        default: Debug.Fail("Painting rotation"); break;
                    }
                    return dtData;
                case 3:
                    switch (dtData)
                    {
                        case EntityPainting.DirectionType.NORTH: return EntityPainting.DirectionType.SOUTH;
                        case EntityPainting.DirectionType.EAST: return EntityPainting.DirectionType.WEST;
                        case EntityPainting.DirectionType.SOUTH: return EntityPainting.DirectionType.NORTH;
                        case EntityPainting.DirectionType.WEST: return EntityPainting.DirectionType.EAST;
                        default: Debug.Fail("Painting rotation"); break;
                    }
                    return dtData;
                default:
                    //Debug.Fail("Painting rotated to default");
                    return dtData;
            }
        }
        public static int RotatePumpkin(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)PumpkinOrientation.NORTH: return (int)PumpkinOrientation.WEST;
                        case (int)PumpkinOrientation.EAST: return (int)PumpkinOrientation.NORTH;
                        case (int)PumpkinOrientation.SOUTH: return (int)PumpkinOrientation.EAST;
                        case (int)PumpkinOrientation.WEST: return (int)PumpkinOrientation.SOUTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)PumpkinOrientation.NORTH: return (int)PumpkinOrientation.EAST;
                        case (int)PumpkinOrientation.EAST: return (int)PumpkinOrientation.SOUTH;
                        case (int)PumpkinOrientation.SOUTH: return (int)PumpkinOrientation.WEST;
                        case (int)PumpkinOrientation.WEST: return (int)PumpkinOrientation.NORTH;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)PumpkinOrientation.NORTH: return (int)PumpkinOrientation.SOUTH;
                        case (int)PumpkinOrientation.EAST: return (int)PumpkinOrientation.WEST;
                        case (int)PumpkinOrientation.SOUTH: return (int)PumpkinOrientation.NORTH;
                        case (int)PumpkinOrientation.WEST: return (int)PumpkinOrientation.EAST;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotateVines(int intData, int intRotation)
        {
            switch (intRotation)
            {
                case 1:
                    switch (intData)
                    {
                        case (int)VineCoverageState.NORTH: return (int)VineCoverageState.WEST;
                        case (int)VineCoverageState.EAST: return (int)VineCoverageState.NORTH;
                        case (int)VineCoverageState.SOUTH: return (int)VineCoverageState.EAST;
                        case (int)VineCoverageState.WEST: return (int)VineCoverageState.SOUTH;
                        case (int)VineCoverageState.TOP: return (int)VineCoverageState.TOP;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 2:
                    switch (intData)
                    {
                        case (int)VineCoverageState.NORTH: return (int)VineCoverageState.EAST;
                        case (int)VineCoverageState.EAST: return (int)VineCoverageState.SOUTH;
                        case (int)VineCoverageState.SOUTH: return (int)VineCoverageState.WEST;
                        case (int)VineCoverageState.WEST: return (int)VineCoverageState.NORTH;
                        case (int)VineCoverageState.TOP: return (int)VineCoverageState.TOP;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                case 3:
                    switch (intData)
                    {
                        case (int)VineCoverageState.NORTH: return (int)VineCoverageState.SOUTH;
                        case (int)VineCoverageState.EAST: return (int)VineCoverageState.WEST;
                        case (int)VineCoverageState.SOUTH: return (int)VineCoverageState.NORTH;
                        case (int)VineCoverageState.WEST: return (int)VineCoverageState.EAST;
                        case (int)VineCoverageState.TOP: return (int)VineCoverageState.TOP;
                        default: Debug.Fail("Invalid switch result"); break;
                    }
                    return intData;
                default:
                    return intData;
            }
        }
        public static int RotateDoor(int intData, int intRotation)
        {
            if (intRotation > 0)
            {
                bool booSwung = false;
                bool booTopHalf = false;
                if (intData >= (int)DoorState.TOPHALF)
                {
                    intData -= (int)DoorState.TOPHALF;
                    booTopHalf = true;
                }
                if (intData >= (int)DoorState.SWUNG)
                {
                    intData -= (int)DoorState.SWUNG;
                    booSwung = true;
                }
                int intDirection = 0;
                switch (intRotation)
                {
                    case 1:
                        switch (intData)
                        {
                            case (int)DoorHinge.NORTHWEST: intDirection = (int)DoorHinge.SOUTHWEST; break;
                            case (int)DoorHinge.NORTHEAST: intDirection = (int)DoorHinge.NORTHWEST; break;
                            case (int)DoorHinge.SOUTHEAST: intDirection = (int)DoorHinge.NORTHEAST; break;
                            case (int)DoorHinge.SOUTHWEST: intDirection = (int)DoorHinge.SOUTHEAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 2:
                        switch (intData)
                        {
                            case (int)DoorHinge.NORTHWEST: intDirection = (int)DoorHinge.NORTHEAST; break;
                            case (int)DoorHinge.NORTHEAST: intDirection = (int)DoorHinge.SOUTHEAST; break;
                            case (int)DoorHinge.SOUTHEAST: intDirection = (int)DoorHinge.SOUTHWEST; break;
                            case (int)DoorHinge.SOUTHWEST: intDirection = (int)DoorHinge.NORTHWEST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    case 3:
                        switch (intData)
                        {
                            case (int)DoorHinge.NORTHWEST: intDirection = (int)DoorHinge.SOUTHEAST; break;
                            case (int)DoorHinge.NORTHEAST: intDirection = (int)DoorHinge.SOUTHWEST; break;
                            case (int)DoorHinge.SOUTHEAST: intDirection = (int)DoorHinge.NORTHWEST; break;
                            case (int)DoorHinge.SOUTHWEST: intDirection = (int)DoorHinge.NORTHEAST; break;
                            default: Debug.Fail("Invalid switch result"); break;
                        }
                        break;
                    default:
                        Debug.WriteLine("Oh noes!");
                        break;
                }
                if (booTopHalf)
                {
                    intDirection += (int)DoorState.TOPHALF;
                }
                if (booSwung)
                {
                    intDirection += (int)DoorState.SWUNG;
                }
                return intDirection;
            }
            else
            {
                return intData;
            }
        }
```