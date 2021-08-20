---
title: 'IVMVirtualMachineEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualMachine 介面的外寄事件介面。
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- IVMVirtualMachineEvents 介面 Virtual PC
- IVMVirtualMachineEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122618"
---
# <a name="ivmvirtualmachineevents-interface"></a>IVMVirtualMachineEvents 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 [**IVMVirtualMachine**](ivmvirtualmachine.md) 介面的外寄事件介面。 用戶端會執行這些方法來接收從 [**IVMVirtualMachine**](ivmvirtualmachine.md)傳送的事件。

## <a name="members"></a>成員

**IVMVirtualMachineEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualMachineEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IVMVirtualMachineEvents** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | 接收可在虛擬機器中使用整合元件的通知。<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | 接收在虛擬機器中卸載整合元件的通知。<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | 接收此虛擬機器設定中的值已變更的通知。<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | 收到通知，表示虛擬機器所需的磁碟空間不足，且虛擬機器無法執行。<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | 收到虛擬機器的增強型影片模式支援已變更的通知。<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | 接收使用者已從客體作業系統登出的通知。<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | 收到客體作業系統已關機的通知。<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | 收到虛擬機器的信號已停止的通知。 這通常表示客體作業系統已損毀。<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | 接收已發出關機要求的通知。<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | 接收已重設虛擬機器的通知。<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | 收到虛擬機器的狀態已變更的通知。<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | 收到虛擬機器有三個錯誤的通知。<br/>                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



 

