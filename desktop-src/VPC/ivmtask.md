---
title: 'IVMTask 介面 (VPCCOMInterfaces .h) '
description: 您可以使用 IVMTask 介面來監視和控制各種 COM 方法的非同步工作。
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- IVMTask 介面 Virtual PC
- IVMTask 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508979"
---
# <a name="ivmtask-interface"></a>IVMTask 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

您可以使用 **IVMTask** 介面來監視和控制各種 COM 方法的非同步工作。

## <a name="members"></a>成員

**IVMTask** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMTask** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMTask** 介面具有這些方法。



| 方法                                                 | 描述                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**取消**](ivmtask-cancel.md)                       | 取消工作。<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | 等候工作完成或指定的逾時間隔。<br/> |



 

### <a name="properties"></a>屬性

**IVMTask** 介面具有這些屬性。



| 屬性                                                        | 存取類型          | Description                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**描述**](ivmtask-description.md)<br/>           | 唯讀<br/> | 工作的描述。<br/>                              |
| [**錯誤**](ivmtask-error.md)<br/>                       | 唯讀<br/> | 此工作所記錄的錯誤。<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | 唯讀<br/> | 針對這項工作記錄的當地語系化錯誤描述。<br/> |
| [**識別碼**](ivmtask-id.md)<br/>                             | 唯讀<br/> | 這項工作的唯一識別碼。<br/>                      |
| [**屬性**](ivmtask-iscancelable.md)<br/>         | 唯讀<br/> | 指出是否可以取消工作。<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | 唯讀<br/> | 指出工作是否已完成。<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | 唯讀<br/> | 工作的完成百分比。<br/>                  |
| [**結果**](ivmtask-result.md)<br/>                     | 唯讀<br/> | 工作的結果。<br/>                                 |



 

## <a name="remarks"></a>備註

可能需要相當長的時間才能完成的方法會傳回 **IVMTask** 物件。 這可讓應用程式監視所需作業的進度，而不需要強制它在等候作業完成時封鎖進一步的執行作業。

下列方法會傳回可用來追蹤進度的 **IVMTask** 物件：

-   [**IVMGuestOS：：登出**](ivmguestos-logoff.md)
-   [**IVMGuestOS：： Restart**](ivmguestos-restart.md)
-   [**IVMGuestOS：： Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk：： Compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk：： Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk：： Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk::MergeTo**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine：： Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine：： Save**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine：： Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine::Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine：： TurnOff**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

