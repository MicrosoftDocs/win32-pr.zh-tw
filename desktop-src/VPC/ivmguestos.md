---
title: 'IVMGuestOS 介面 (VPCCOMInterfaces .h) '
description: 定義在虛擬機器內執行的客體作業系統。
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- IVMGuestOS 介面 Virtual PC
- IVMGuestOS 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b52d4f7651a21b1baad31448e47866dfb5bf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105815"
---
# <a name="ivmguestos-interface"></a>IVMGuestOS 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義在虛擬機器內執行的客體作業系統。 此介面可讓您與在客體作業系統內執行的整合元件互動。 您可以使用 [**IVMVirtualMachine：： GuestOS**](ivmvirtualmachine-guestos.md)屬性來抓取虛擬機器的 **IVMGuestOS** 。

## <a name="members"></a>成員

**IVMGuestOS** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMGuestOS** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMGuestOS** 介面具有這些方法。



| 方法                                                                          | 描述                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | 抓取虛擬機器中執行之客體作業系統的版本資訊。<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | 抓取來賓內的具名引數。<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | 找出最新的整合元件，並將其安裝在客體作業系統中。<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | 判斷要求的會話是否存在。<br/>                                         |
| [**登出**](ivmguestos-logoff.md)                                             | 登出客體作業系統中的所有使用者。<br/>                                          |
| [**重新啟動**](ivmguestos-restart.md)                                           | 重新開機客體作業系統。<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | 設定來賓內的具名引數。<br/>                                                     |
| [**關閉**](ivmguestos-shutdown.md)                                         | 關閉客體作業系統。<br/>                                                       |



 

### <a name="properties"></a>屬性

**IVMGuestOS** 介面具有這些屬性。



| 屬性                                                                                   | 存取類型           | Description                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | 唯讀<br/>  | 指出是否可以完全關閉客體作業系統 (需要) 整合元件。<br/>                         |
| [**名稱**](ivmguestos-computername.md)<br/>                                 | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的電腦名稱稱。<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | 唯讀<br/>  | 虛擬機器中執行的客體作業系統 CSDVersion。<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | 唯讀<br/>  | 過去一分鐘收到的預期心跳量百分比。<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | 唯讀<br/>  | 在客體作業系統中安裝之整合元件的版本。<br/>                                               |
| [**IsHeartbeating**](ivmguestos-isheartbeating.md)<br/>                             | 唯讀<br/>  | 指出虛擬機器是否有信號。<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | 讀取/寫入<br/> | 指出此虛擬機器中的整合元件是否應將來賓的時鐘與主機的時鐘同步。<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | 唯讀<br/>  | 指出是否允許在客體作業系統中同時使用多個使用者會話。<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的組建編號。<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的主要版本。<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的次要版本。<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | 唯讀<br/>  | 虛擬機器中執行的客體作業系統名稱。<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的平臺識別碼。<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | 唯讀<br/>  | 在虛擬機器中執行的客體作業系統版本。<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的產品類型。<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | 唯讀<br/>  | 指出是否已在客體作業系統中鎖定畫面。<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | 唯讀<br/>  | 虛擬機器中執行的客體作業系統之 service pack 的主要版本。<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | 唯讀<br/>  | 虛擬機器中執行之客體作業系統的 service pack 次要版本。<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | 唯讀<br/>  | 虛擬機器中執行的客體作業系統 SuiteMask。<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | 唯讀<br/>  | 客體作業系統中遠端桌面服務所使用的埠。<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | 唯讀<br/>  | 客體作業系統中終端機服務初始化的狀態。<br/>                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



 

