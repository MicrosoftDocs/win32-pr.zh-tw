---
title: 'IVMParallelPortCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的平行埠集合。 若要取得 IVMParallelPortCollection 物件，請使用 IVMVirtualMachine ParallelPorts 屬性。
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- IVMParallelPortCollection 介面 Virtual PC
- IVMParallelPortCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106050"
---
# <a name="ivmparallelportcollection-interface"></a>IVMParallelPortCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內的平行埠集合。 若要取得 **IVMParallelPortCollection** 物件，請使用 [**IVMVirtualMachine：:P arallelports**](ivmvirtualmachine-parallelports.md) 屬性。

## <a name="members"></a>成員

**IVMParallelPortCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMParallelPortCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMParallelPortCollection** 介面具有這些屬性。



| 屬性                                                           | 存取類型          | Description                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmparallelportcollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                 |
| [**計數**](ivmparallelportcollection-count.md)<br/>        | 唯讀<br/> | 此集合中的平行埠數目。<br/>                  |
| [**項目**](ivmparallelportcollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的平行埠物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection 定義為27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMVirtualMachine：:P arallelPorts**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

