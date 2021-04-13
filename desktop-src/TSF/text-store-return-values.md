---
title: '文字存放區傳回值 (Textstor) '
description: 當檔管理員處理文字存放區時，它會從0xHHHH0200 到0xHHHH0300 的範圍內產生傳回值。 下表依字母順序列出文字存放區的傳回值。
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508991"
---
# <a name="text-store-return-values"></a><span data-ttu-id="06968-104">文字存放區傳回值</span><span class="sxs-lookup"><span data-stu-id="06968-104">Text Store Return Values</span></span>

<span data-ttu-id="06968-105">當檔管理員處理文字存放區時，它會從 0x *hhhh hhhh* 0200 到 0x *hhhh hhhh* 0300 的範圍產生傳回值。</span><span class="sxs-lookup"><span data-stu-id="06968-105">When a document manager processes a text store, it produces return values in the range from 0x *HHHH* 0200 through 0x *HHHH* 0300.</span></span> <span data-ttu-id="06968-106">下表依字母順序列出文字存放區的傳回值。</span><span class="sxs-lookup"><span data-stu-id="06968-106">The following table lists text store return values in alphabetical order.</span></span>



| <span data-ttu-id="06968-107">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="06968-107">Return code/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="06968-108">Description</span><span class="sxs-lookup"><span data-stu-id="06968-108">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <span data-ttu-id="06968-109"><dt>**TS \_E \_ FORMAT**</dt> <dt>0x8004020a</dt></span><span class="sxs-lookup"><span data-stu-id="06968-109"><dt>**TS\_E\_FORMAT**</dt> <dt>0x8004020a</dt></span></span> </dl>                   | <span data-ttu-id="06968-110">應用程式不支援使用 [**ITextStoreACP：： InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)來插入 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject)物件中所包含的資料類型。</span><span class="sxs-lookup"><span data-stu-id="06968-110">Application does not support the data type contained in the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) object to be inserted using [**ITextStoreACP::InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).</span></span><br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <span data-ttu-id="06968-111"><dt>**TS \_E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt></span><span class="sxs-lookup"><span data-stu-id="06968-111"><dt>**TS\_E\_INVALIDPOINT**</dt> <dt>0x80040207</dt></span></span> </dl> | <span data-ttu-id="06968-112">參數不在任何字元的周框方塊內。</span><span class="sxs-lookup"><span data-stu-id="06968-112">Parameter is not within the bounding box of any character.</span></span><br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <span data-ttu-id="06968-113"><dt>**TS \_E \_ INVALIDPOS**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="06968-113"><dt>**TS\_E\_INVALIDPOS**</dt> <dt>0x80040200</dt></span></span> </dl>       | <span data-ttu-id="06968-114">指定的範圍會延伸至檔之外。</span><span class="sxs-lookup"><span data-stu-id="06968-114">Range specified extends outside the document.</span></span><br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <span data-ttu-id="06968-115"><dt>**TS \_E \_ NOINTERFACE**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="06968-115"><dt>**TS\_E\_NOINTERFACE**</dt> <dt>0x80040204</dt></span></span> </dl>    | <span data-ttu-id="06968-116">物件不支援要求的介面。</span><span class="sxs-lookup"><span data-stu-id="06968-116">Object does not support the requested interface.</span></span><br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <span data-ttu-id="06968-117"><dt>**TS \_E \_ NOLAYOUT**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="06968-117"><dt>**TS\_E\_NOLAYOUT**</dt> <dt>0x80040206</dt></span></span> </dl>             | <span data-ttu-id="06968-118">應用程式尚未計算文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="06968-118">Application has not calculated a text layout.</span></span><br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <span data-ttu-id="06968-119"><dt>**TS \_E \_ NOLOCK**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="06968-119"><dt>**TS\_E\_NOLOCK**</dt> <dt>0x80040201</dt></span></span> </dl>                   | <span data-ttu-id="06968-120">應用程式沒有檔的唯讀鎖定或讀取/寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="06968-120">Application does not have a read-only lock or read/write lock for the document.</span></span><br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <span data-ttu-id="06968-121"><dt>**TS \_E \_ NOOBJECT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="06968-121"><dt>**TS\_E\_NOOBJECT**</dt> <dt>0x80040202</dt></span></span> </dl>             | <span data-ttu-id="06968-122">內嵌的內容位移未放置於 TF \_ 字元 \_ 內嵌字元之前。</span><span class="sxs-lookup"><span data-stu-id="06968-122">Embedded content offset is not positioned before a TF\_CHAR\_EMBEDDED character.</span></span><br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <span data-ttu-id="06968-123"><dt>**TS \_E \_ NOSELECTION**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="06968-123"><dt>**TS\_E\_NOSELECTION**</dt> <dt>0x80040205</dt></span></span> </dl>    | <span data-ttu-id="06968-124">檔沒有選取專案。</span><span class="sxs-lookup"><span data-stu-id="06968-124">Document has no selection.</span></span><br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <span data-ttu-id="06968-125"><dt>**TS \_E \_ NOSERVICE**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="06968-125"><dt>**TS\_E\_NOSERVICE**</dt> <dt>0x80040203</dt></span></span> </dl>          | <span data-ttu-id="06968-126">無法傳回內容以符合服務 GUID。</span><span class="sxs-lookup"><span data-stu-id="06968-126">Content cannot be returned to match the service GUID.</span></span><br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <span data-ttu-id="06968-127"><dt>**TS \_E \_ READONLY**</dt> <dt>0x80040209</dt></span><span class="sxs-lookup"><span data-stu-id="06968-127"><dt>**TS\_E\_READONLY**</dt> <dt>0x80040209</dt></span></span> </dl>             | <span data-ttu-id="06968-128">檔是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="06968-128">Document is read-only.</span></span> <span data-ttu-id="06968-129">無法修改內容。</span><span class="sxs-lookup"><span data-stu-id="06968-129">Cannot modify content.</span></span><br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <span data-ttu-id="06968-130"><dt>**TS \_E \_ 同步**</dt> <dt>0x00040300</dt></span><span class="sxs-lookup"><span data-stu-id="06968-130"><dt>**TS\_E\_SYNCHRONOUS**</dt> <dt>0x00040300</dt></span></span> </dl>    | <span data-ttu-id="06968-131">無法同步鎖定檔。</span><span class="sxs-lookup"><span data-stu-id="06968-131">Document cannot be locked synchronously.</span></span><br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <span data-ttu-id="06968-132"><dt>**TS \_S \_ ASYNC**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="06968-132"><dt>**TS\_S\_ASYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                         | <span data-ttu-id="06968-133">檔已成功接收非同步鎖定。</span><span class="sxs-lookup"><span data-stu-id="06968-133">Document successfully received an asynchronous lock.</span></span><br/>                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="06968-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="06968-134">Requirements</span></span>



| <span data-ttu-id="06968-135">需求</span><span class="sxs-lookup"><span data-stu-id="06968-135">Requirement</span></span> | <span data-ttu-id="06968-136">值</span><span class="sxs-lookup"><span data-stu-id="06968-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06968-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06968-137">Minimum supported client</span></span><br/> | <span data-ttu-id="06968-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06968-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="06968-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06968-139">Minimum supported server</span></span><br/> | <span data-ttu-id="06968-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06968-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06968-141">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="06968-141">Redistributable</span></span><br/>          | <span data-ttu-id="06968-142">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="06968-142">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="06968-143">標頭</span><span class="sxs-lookup"><span data-stu-id="06968-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="06968-144"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="06968-144"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="06968-145">Idl</span><span class="sxs-lookup"><span data-stu-id="06968-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06968-146"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="06968-146"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06968-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06968-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06968-148">**ITextStoreACP：： InsertEmbedded**</span><span class="sxs-lookup"><span data-stu-id="06968-148">**ITextStoreACP::InsertEmbedded**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

