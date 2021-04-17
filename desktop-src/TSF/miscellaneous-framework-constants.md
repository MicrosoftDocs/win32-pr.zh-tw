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
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="8a2fd-103">其他架構常數</span><span class="sxs-lookup"><span data-stu-id="8a2fd-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="8a2fd-104">其他架構常數表示用戶端、進程或文字的設定。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="8a2fd-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="8a2fd-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8a2fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="8a2fd-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="8a2fd-107"><dt>**TF \_CLIENTID \_ Null**</dt> <dt> ( (TfClientId) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="8a2fd-108">指出用戶端已停用的文字服務。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="8a2fd-109">請參閱 [TfClientId](tfclientid.md)。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="8a2fd-110"><dt>**TF \_不正確 \_ GUIDATOM**</dt> <dt> ( (TfGuidAtom) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="8a2fd-111">目前進程的 [TfGuidAtom](tfguidatom.md) 值無效。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="8a2fd-112"><dt>**TF \_預設 \_ 選取**</dt> <dt> ( TS \_ 預設 \_ 選取範圍 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="8a2fd-113">使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-113">Use the default selection.</span></span> <span data-ttu-id="8a2fd-114">用於 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)、 [ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)和 [ITextStoreAnchor：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="8a2fd-115"><dt>**TF \_GTP \_ 包括 \_ 文字**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="8a2fd-116">指定 [ITfEditRecord：： GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) 方法會取得範圍物件的集合，這些物件涵蓋編輯會話期間所變更的文字。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="8a2fd-117"><dt>**TF \_HF \_ 物件**</dt> <dt> ( 1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="8a2fd-118">如果遇到内嵌物件，範圍排班就會停止。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="8a2fd-119">用於 [TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)結構的 **dwFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="8a2fd-120"><dt>**TF \_IE \_ 更正**</dt> <dt> ( 1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="8a2fd-121">文字是現有內容的轉換 (更正) ，因此其他文字服務可以保留與原始文字相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="8a2fd-122">在 [ITfRange：： InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)的 *dwFlags* 參數中使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="8a2fd-123"><dt>**TF \_不正確 \_ COOKIE**</dt> <dt> ( 0xffffffff )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="8a2fd-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="8a2fd-125"><dt>**TF \_不正確 \_ 編輯 \_ COOKIE**</dt> <dt> ( 0 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="8a2fd-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="8a2fd-127"><dt>**TF \_POPF \_ 所有**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="8a2fd-128">所有內容都會從堆疊中移除。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="8a2fd-129">用於 [ITfDocumentMgr：:P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)的 *dwFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="8a2fd-130"><dt>**TF \_ST \_ 更正**</dt> <dt> ( 1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="8a2fd-131">文字是現有內容的轉換 (更正) ，因此其他文字服務可以保留與原始文字相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="8a2fd-132">在 [ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)的 *dwFlags* 參數中使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="8a2fd-133"><dt>**TF \_TU \_ 更正**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="8a2fd-134">文字變更是現有內容的轉換 (更正) 的結果。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="8a2fd-135">這表示文字的語義未變更。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="8a2fd-136">在 [ITfPropertyStore：： OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)的 *dwFlags* 參數中使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="8a2fd-137"><dt>**TF \_US \_ HIDETIPUI**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="8a2fd-138">未使用。</span><span class="sxs-lookup"><span data-stu-id="8a2fd-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="8a2fd-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a2fd-139">Requirements</span></span>



| <span data-ttu-id="8a2fd-140">需求</span><span class="sxs-lookup"><span data-stu-id="8a2fd-140">Requirement</span></span> | <span data-ttu-id="8a2fd-141">值</span><span class="sxs-lookup"><span data-stu-id="8a2fd-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2fd-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a2fd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2fd-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a2fd-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8a2fd-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a2fd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2fd-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a2fd-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a2fd-146">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a2fd-146">Redistributable</span></span><br/>          | <span data-ttu-id="8a2fd-147">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="8a2fd-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="8a2fd-148">標頭</span><span class="sxs-lookup"><span data-stu-id="8a2fd-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a2fd-149"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a2fd-150">Idl</span><span class="sxs-lookup"><span data-stu-id="8a2fd-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a2fd-151"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a2fd-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a2fd-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a2fd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2fd-153">ITextStoreACP：： GetSelection</span><span class="sxs-lookup"><span data-stu-id="8a2fd-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="8a2fd-154">ITextStoreAnchor::GetSelection</span><span class="sxs-lookup"><span data-stu-id="8a2fd-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="8a2fd-155">ITfCoNtext：： GetSelection</span><span class="sxs-lookup"><span data-stu-id="8a2fd-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="8a2fd-156">ITfDocumentMgr：:P op</span><span class="sxs-lookup"><span data-stu-id="8a2fd-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="8a2fd-157">ITfEditRecord::GetTextAndPropertyUpdates</span><span class="sxs-lookup"><span data-stu-id="8a2fd-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="8a2fd-158">ITfPropertyStore::OnTextUpdated</span><span class="sxs-lookup"><span data-stu-id="8a2fd-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="8a2fd-159">ITfRange::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="8a2fd-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="8a2fd-160">ITfRange：： SetText</span><span class="sxs-lookup"><span data-stu-id="8a2fd-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="8a2fd-161">TfClientId</span><span class="sxs-lookup"><span data-stu-id="8a2fd-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="8a2fd-162">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="8a2fd-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="8a2fd-163">TF \_ HALTCOND</span><span class="sxs-lookup"><span data-stu-id="8a2fd-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





