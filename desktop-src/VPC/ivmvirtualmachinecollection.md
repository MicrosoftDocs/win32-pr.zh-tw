---
title: 'IVMVirtualMachineCollection 介面 (VPCCOMInterfaces .h) '
description: 定義 Windows Virtual PC 中的虛擬機器集合。 若要取得 IVMVirtualMachineCollection 物件，請使用 IVMVirtualPC VirtualMachines 屬性。
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- IVMVirtualMachineCollection 介面 Virtual PC
- IVMVirtualMachineCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105647"
---
# <a name="ivmvirtualmachinecollection-interface"></a>IVMVirtualMachineCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 Windows Virtual PC 中的虛擬機器集合。 若要取得 **IVMVirtualMachineCollection** 物件，請使用 [**IVMVirtualPC：： VirtualMachines**](ivmvirtualpc-virtualmachines.md) 屬性。

## <a name="members"></a>成員

**IVMVirtualMachineCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualMachineCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMVirtualMachineCollection** 介面具有這些屬性。



| 屬性                                                             | 存取類型          | Description                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                   |
| [**計數**](ivmvirtualmachinecollection-count.md)<br/>        | 唯讀<br/> | 此集合中的虛擬機器數目。<br/>                  |
| [**項目**](ivmvirtualmachinecollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的虛擬機器物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                           |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection 定義為 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC：： VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

