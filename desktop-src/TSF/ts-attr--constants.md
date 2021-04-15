---
title: 'TS_ATTR_ 常數 (Textstor) '
description: TS \_ ATTR \_ \ 常數可用來取得和變更檔案屬性的值。 這些常數會在 ITextStoreACP 和 ITextStoreAnchor 方法中形成可能的等位旗標值。
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466161"
---
# <a name="ts_attr_-constants"></a>TS \_ ATTR \_ \* 常數

TS \_ ATTR \_ \* 常數可用來取得和變更 document 屬性的值。 這些常數會在 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 和 [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) 方法中形成可能的等位旗標值。



| 常數/值                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ATTR \_ 找到 \_**</dt>回溯 <dt> ( 0x1 )</dt> </dl>        | 從開始字元或錨點位置向後搜尋，以取得轉換在檔案屬性值中發生的位置。 預設值為「向前搜尋」。<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ATTR \_ FIND \_ 需要 \_ OFFSET**</dt> <dt> ( 0x2 )</dt> </dl> | 傳回開始字元或錨點位置之間的字元數 (**acpStart** 在 [ITextStoreACP：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) 或 **PaStart** in [ITextStoreAnchor：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) 和發生屬性轉換的位置。<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ATTR \_ FIND \_ UPDATESTART**</dt> <dt> ( 0x4 )</dt> </dl>  | 供 [ITextStoreAnchor：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) 在下一個屬性轉換時放置輸入錨點（如果找到的話）。 否則，不會修改輸入錨點。<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ATTR \_ 尋找 \_ 想要的 \_ 值**</dt> <dt> ( 0x8 )</dt> </dl>    | 將支援的檔案屬性值載入 [TS \_ ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) 結構。<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ATTR \_ FIND \_ 需要 \_ END**</dt> <dt> ( 0x10 )</dt> </dl>         | 供 [ITextStoreACP：： RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) 和 [ITextStoreAnchor：： RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) 用來取得以指定的字元或錨點位置結尾的檔案屬性值。<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ATTR \_ FIND \_ HIDDEN**</dt> <dt> ( 0x20 )</dt> </dl>                | 保留的。<br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[TS \_ ATTRID](ts-attrid.md)
</dt> <dt>

[TS \_ ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP：： FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP：： RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





