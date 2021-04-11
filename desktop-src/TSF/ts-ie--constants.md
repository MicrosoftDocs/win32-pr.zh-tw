---
title: 'TS_IE_ 常數 (Textstor) '
description: TS \_ IE \_ \ 常數描述如何插入可包含文字服務所使用之内嵌物件的文字。
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094231"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="ca275-103">TS \_ IE \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="ca275-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="ca275-104">TS \_ IE \_ \* 常數描述如何插入可包含文字服務所使用之内嵌物件的文字。</span><span class="sxs-lookup"><span data-stu-id="ca275-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="ca275-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ca275-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="ca275-106">Description</span><span class="sxs-lookup"><span data-stu-id="ca275-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="ca275-107"><dt>**TS \_IE \_ 更正**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="ca275-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="ca275-108">文字是現有內容的轉換 (更正) ，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔案資料或語言識別項。</span><span class="sxs-lookup"><span data-stu-id="ca275-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="ca275-109"><dt>**TS \_IE \_ 組合**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="ca275-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="ca275-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="ca275-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="ca275-111">備註</span><span class="sxs-lookup"><span data-stu-id="ca275-111">Remarks</span></span>

<span data-ttu-id="ca275-112">這些常數會用在 [ITextStoreACP：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)和 [ITextStoreAnchor：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)的 *dwFlags* 參數中。</span><span class="sxs-lookup"><span data-stu-id="ca275-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca275-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca275-113">Requirements</span></span>



| <span data-ttu-id="ca275-114">需求</span><span class="sxs-lookup"><span data-stu-id="ca275-114">Requirement</span></span> | <span data-ttu-id="ca275-115">值</span><span class="sxs-lookup"><span data-stu-id="ca275-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca275-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca275-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca275-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca275-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca275-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca275-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca275-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca275-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca275-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ca275-120">Redistributable</span></span><br/>          | <span data-ttu-id="ca275-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="ca275-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ca275-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ca275-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca275-123"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca275-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca275-124">Idl</span><span class="sxs-lookup"><span data-stu-id="ca275-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca275-125"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca275-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca275-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca275-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca275-127">ITextStoreACP：： InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="ca275-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="ca275-128">ITextStoreAnchor::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="ca275-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





