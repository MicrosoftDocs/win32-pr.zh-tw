---
title: 'IVMTaskCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至指定之索引的工作物件。
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMTaskCollection 介面
- IVMTaskCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508980"
---
# <a name="ivmtaskcollectionitem-property"></a>IVMTaskCollection：： Item 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取對應至指定之索引的工作物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a>屬性值

[**IVMTask**](ivmtask.md)物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。 <br/>                                                      |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | *Task* 參數為 **Null**。 <br/>                                                  |
| <dl> <dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | 要求專案的索引未對應到此集合中的專案。 <br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                   |



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

[**IVMTaskCollection**](ivmtaskcollection.md)
</dt> </dl>

 

