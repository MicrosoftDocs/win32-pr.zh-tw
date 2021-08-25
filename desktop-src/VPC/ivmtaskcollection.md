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
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958798"
---
# <a name="ivmtaskcollection-interface"></a>IVMTaskCollection 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義工作物件的集合。 若要取得 **IVMTaskCollection** 物件，請使用 [**IVMVirtualPC：： Tasks**](ivmvirtualpc-tasks.md) 屬性。

## <a name="members"></a>成員

**IVMTaskCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMTaskCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMTaskCollection** 介面具有這些屬性。



| 屬性                                                   | 存取類型          | 描述                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                        |
| [**計數**](ivmtaskcollection-count.md)<br/>        | 唯讀<br/> | 這個集合中的工作數目。<br/>                  |
| [**項目**](ivmtaskcollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的 task 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
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

 

