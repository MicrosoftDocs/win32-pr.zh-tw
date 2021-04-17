---
title: '其他架構常數 (Msctf .h) '
description: 其他架構常數表示用戶端、進程或文字的設定。
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466445"
---
# <a name="miscellaneous-framework-constants"></a>其他架構常數

其他架構常數表示用戶端、進程或文字的設定。



| 常數/值                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_CLIENTID \_ Null**</dt> <dt> ( (TfClientId) 0)</dt> </dl>                        | 指出用戶端已停用的文字服務。 請參閱 [TfClientId](tfclientid.md)。<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_不正確 \_ GUIDATOM**</dt> <dt> ( (TfGuidAtom) 0)</dt> </dl>               | 目前進程的 [TfGuidAtom](tfguidatom.md) 值無效。<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_預設 \_ 選取**</dt> <dt> ( TS \_ 預設 \_ 選取範圍 )</dt> </dl> | 使用預設選項。 用於 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)、 [ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)和 [ITextStoreAnchor：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)。<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_GTP \_ 包括 \_ 文字**</dt> <dt> ( 0x1 )</dt> </dl>                               | 指定 [ITfEditRecord：： GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) 方法會取得範圍物件的集合，這些物件涵蓋編輯會話期間所變更的文字。<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_HF \_ 物件**</dt> <dt> ( 1 )</dt> </dl>                                              | 如果遇到内嵌物件，範圍排班就會停止。 用於 [TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)結構的 **dwFlags** 成員。<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_IE \_ 更正**</dt> <dt> ( 1 )</dt> </dl>                                  | 文字是現有內容的轉換 (更正) ，因此其他文字服務可以保留與原始文字相關聯的資料。 在 [ITfRange：： InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)的 *dwFlags* 參數中使用。<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_不正確 \_ COOKIE**</dt> <dt> ( 0xffffffff )</dt> </dl>                      | 未使用。<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_不正確 \_ 編輯 \_ COOKIE**</dt> <dt> ( 0 )</dt> </dl>               | 未使用。<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_POPF \_ 所有**</dt> <dt> ( 0x1 )</dt> </dl>                                               | 所有內容都會從堆疊中移除。 用於 [ITfDocumentMgr：:P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)的 *dwFlags* 參數。<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ST \_ 更正**</dt> <dt> ( 1 )</dt> </dl>                                  | 文字是現有內容的轉換 (更正) ，因此其他文字服務可以保留與原始文字相關聯的資料。 在 [ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)的 *dwFlags* 參數中使用。<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_TU \_ 更正**</dt> <dt> ( 0x1 )</dt> </dl>                                | 文字變更是現有內容的轉換 (更正) 的結果。 這表示文字的語義未變更。 在 [ITfPropertyStore：： OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)的 *dwFlags* 參數中使用。<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | 未使用。<br/>                                                                                                                                                                                                                                          |



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

[ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr：:P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





