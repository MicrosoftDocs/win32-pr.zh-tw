---
title: 'IVMHardDiskConnectionCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的硬碟連接集合。 若要取得 IVMHardDiskConnectionCollection 物件，請使用 IVMVirtualMachine HardDiskConnections 屬性。
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- IVMHardDiskConnectionCollection 介面 Virtual PC
- IVMHardDiskConnectionCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464185"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>IVMHardDiskConnectionCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內的硬碟連接集合。 若要取得 **IVMHardDiskConnectionCollection** 物件，請使用 [**IVMVirtualMachine：： HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) 屬性。

## <a name="members"></a>成員

**IVMHardDiskConnectionCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMHardDiskConnectionCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMHardDiskConnectionCollection** 介面具有這些屬性。



| 屬性                                                                 | 存取類型          | Description                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                        |
| [**計數**](ivmharddiskconnectioncollection-count.md)<br/>        | 唯讀<br/> | 此集合中的硬碟連接數目。<br/>                  |
| [**項目**](ivmharddiskconnectioncollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的硬碟連線物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                          |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                               |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                      |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection 定義為 b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

