---
title: 'TF_IAS_ 常數 (Msctf) '
description: TF \_ IAS \_ \ 常數是在方法中用來做為位旗標，這些旗標會在選取範圍或插入點插入文字或內嵌的物件。
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999813"
---
# <a name="tf_ias_-constants"></a>TF \_ IAS \_ \* 常數

TF \_ IAS \_ \* 常數是在方法中用來做為位旗標，這些旗標會在選取範圍或插入點插入文字或內嵌的物件。



| 常數/值                                                                                                                                                                                                                                                                       | Description                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**TF \_IAS \_ NOQUERY**</dt> <dt> ( 0x1 )</dt> </dl>                                                       | 在結束時插入文字，範圍指標會設定為 **Null** 。 無法與 TF \_ IAS QUERYONLY 旗標合併使用 \_ 。<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**TF \_IAS \_ QUERYONLY**</dt> <dt> ( 0x2 )</dt> </dl>                                                 | 請勿執行插入。 呼叫端只需要設定範圍指標。 無法與 TF \_ IAS NOQUERY 旗標合併使用 \_ 。<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**TF \_IAS \_ 沒有 \_ 預設 \_ 組合**</dt> <dt> ( 0x80000000 )</dt> </dl> | 如果需要組合，TSF 將不會建立預設的組合。 呼叫端必須在範圍內開始撰寫。<br/>         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITextStoreACP：： InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP：： InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[ITextStoreAnchor::InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[ITextStoreAnchor::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertTextAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





