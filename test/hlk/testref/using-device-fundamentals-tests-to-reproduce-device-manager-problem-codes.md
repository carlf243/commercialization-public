# Using Device Fundamentals Tests to Reproduce Device Manager Problem Codes

The Device Fundamentals (DevFund) tests use Microsoft-supplied I/O plug-ins to exercise devices by sending device class-specific I/O to the device while disabling and enabling the device, cycling the system through power states and reboots, deallocating and reallocating resources, and other tasks.

The following table matches device problem codes to tests known to exercise a device in such a way as to induce the corresponding problem code. This chart can be used be device and driver testers in an attempt to reproduce device problems seen in the wild, or problems which may be hard to reproduce during regular testing.

| **Device Error Code**        | **Device Error Message**             | **Device Fundamentals Test**                   |                             
|------------------------------|--------------------------------------|------------------------------------------------|
| [10](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-start) | [CM\_PROB\_FAILED\_START](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-start)| [DF - PNP Rebalance Fail Restart Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn941789(v=vs.85).aspx)<br>[DF - PNP Surprise Remove Device Test (Development and Integration)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn940526(v=vs.85).aspx)<br>[DF - PNP Surprise Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn941905(v=vs.85).aspx)<br>[DF - Reboot restart with IO before and after (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929617(v=vs.85).aspx)<br>[DF - PNP Cancel Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929340(v=vs.85).aspx)<br>[DF - PNP Disable And Enable Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929657(v=vs.85).aspx)<br>[DF - PNP Rebalance Request New Resources Device Test (Development and Integration)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn942119(v=vs.85).aspx)<br>[DF - PNP Rebalance Request New Resources Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn941596(v=vs.85).aspx)<br>[DF - PNP Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn942064(v=vs.85).aspx)<br>[DF - PNP Stop (Rebalance) Device Test (Development and Integration)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn941324(v=vs.85).aspx)<br>[DF - PNP Stop (Rebalance) Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn940665(v=vs.85).aspx)<br>           [DF - Sleep with IO During (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929660(v=vs.85).aspx)<br>[DF - PCI Root Port Surprise Remove Test (PCI devices only) (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn942131(v=vs.85).aspx)            |
| [14](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-need-restart)               | [CM\_PROB\_NEED\_RESTART](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-need-restart)                               | [DF - PNP Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn942064(v=vs.85).aspx)<br>           [DF - PNP DIF Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929420(v=vs.85).aspx)                                       |
| [28](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-install)             | [CM\_PROB\_FAILED\_INSTALL](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-install)                           | [DF - PNP DIF Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929420(v=vs.85).aspx)                                      |
| [38](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-driver-failed-prior-unload) | [CM\_PROB\_DRIVER\_FAILED\_PRIOR\_UNLOAD](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-driver-failed-prior-unload) | [DF - PNP DIF Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929420(v=vs.85).aspx)                                      |
| [39](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-driver-failed-load)         | [CM\_PROB\_DRIVER\_FAILED\_LOAD](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-driver-failed-load)                  | [DF - PNP DIF Remove Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929420(v=vs.85).aspx)                                      |
| [43](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-post-start)          | [CM\_PROB\_FAILED\_POST\_START](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-failed-post-start)                    | [DF - Sleep with IO During (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929660(v=vs.85).aspx)                                            |
| [52](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-unsigned-driver)            | [CM\_PROB\_UNSIGNED\_DRIVER](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/cm-prob-unsigned-driver)                         | [DF - PNP Disable And Enable Device Test (Reliability)](https://msdn.microsoft.com/en-us/library/windows/hardware/dn929657(v=vs.85).aspx)                              |

See [Device Manager Error Messages](https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-manager-error-messages) for the list of device error codes.

See [Device.DevFund tests](https://msdn.microsoft.com/en-us/library/windows/hardware/dn941915(v=vs.85).aspx) for the complete list of Device Fundamentals tests.