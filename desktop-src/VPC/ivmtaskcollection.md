---
title: 'IVMTaskCollection 介面 (VPCCOMInterfaces .h) '
description: 定義工作物件的集合。 若要取得 IVMTaskCollection 物件，請使用 IVMVirtualPC Tasks 屬性。
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- IVMTaskCollection 介面 Virtual PC
- IVMTaskCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385042"
---
# <a name="ivmtaskcollection-interface"></a>IVMTaskCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義工作物件的集合。 若要取得 **IVMTaskCollection** 物件，請使用 [**IVMVirtualPC：： Tasks**](ivmvirtualpc-tasks.md) 屬性。

## <a name="members"></a>成員

**IVMTaskCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMTaskCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMTaskCollection** 介面具有這些屬性。



| 屬性                                                   | 存取類型          | Description                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                        |
| [**計數**](ivmtaskcollection-count.md)<br/>        | 唯讀<br/> | 這個集合中的工作數目。<br/>                  |
| [**項目**](ivmtaskcollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的 task 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection 定義為5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC：： Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

