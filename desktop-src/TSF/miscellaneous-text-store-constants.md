---
title: '其他文字存放區常數 (Textstor .h) '
description: 其他的文字存放區常數會設定文字存放區的特定屬性。
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105401"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="1ef68-103">其他文字存放區常數</span><span class="sxs-lookup"><span data-stu-id="1ef68-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="1ef68-104">其他的文字存放區常數會設定文字存放區的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="1ef68-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="1ef68-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="1ef68-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="1ef68-106">Description</span><span class="sxs-lookup"><span data-stu-id="1ef68-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="1ef68-107"><dt>**TS \_預設 \_ 選項**</dt> <dt> ( ( ULONG ) -1 )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="1ef68-108">如果 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)的 *ulIndex* 參數設定為此值，則會取得預設的選取專案。</span><span class="sxs-lookup"><span data-stu-id="1ef68-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="1ef68-109"><dt>**TS \_GEA \_ HIDDEN**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="1ef68-110">如果 [ITextStoreAnchor：： GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)的 *dwFlags* 參數設定為此值，則内嵌物件可以位於隱藏文字內。</span><span class="sxs-lookup"><span data-stu-id="1ef68-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="1ef68-111"><dt>**TS \_GTA \_ HIDDEN**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="1ef68-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="1ef68-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="1ef68-113"><dt>**TS \_ST \_ 更正**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="1ef68-114">如果 [ITextStoreACP：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)、 [ITextStoreAnchor：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)或 [ITextStoreACPSink：： OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)的 *dwFlags* 參數設定為此值，則文字會是 () 更正現有內容的轉換，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔資料或語言識別項。</span><span class="sxs-lookup"><span data-stu-id="1ef68-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="1ef68-115"><dt>**TS \_TC \_ 更正**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="1ef68-116">如果 [ITextStoreAnchorSink：： OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)的 *dwFlags* 參數設定為此值，則文字會是 () 更正現有內容的轉換，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔案資料或語言識別項。</span><span class="sxs-lookup"><span data-stu-id="1ef68-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="1ef68-117"><dt>**TS \_VCOOKIE \_ NUL**</dt> <dt> ( 0xffffffff )</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="1ef68-118">由 TSF 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="1ef68-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="1ef68-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ef68-119">Requirements</span></span>



| <span data-ttu-id="1ef68-120">需求</span><span class="sxs-lookup"><span data-stu-id="1ef68-120">Requirement</span></span> | <span data-ttu-id="1ef68-121">值</span><span class="sxs-lookup"><span data-stu-id="1ef68-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef68-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ef68-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef68-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef68-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ef68-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ef68-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef68-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef68-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ef68-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1ef68-126">Redistributable</span></span><br/>          | <span data-ttu-id="1ef68-127">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="1ef68-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="1ef68-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1ef68-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef68-129"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ef68-130">Idl</span><span class="sxs-lookup"><span data-stu-id="1ef68-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ef68-131"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ef68-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef68-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ef68-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef68-133">ITfCoNtext：： GetSelection</span><span class="sxs-lookup"><span data-stu-id="1ef68-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="1ef68-134">ITextStoreACP：： SetText</span><span class="sxs-lookup"><span data-stu-id="1ef68-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="1ef68-135">ITextStoreAnchor：： SetText</span><span class="sxs-lookup"><span data-stu-id="1ef68-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="1ef68-136">ITextStoreAnchor::GetEmbedded</span><span class="sxs-lookup"><span data-stu-id="1ef68-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="1ef68-137">ITextStoreACPSink：： OnTextChange</span><span class="sxs-lookup"><span data-stu-id="1ef68-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="1ef68-138">ITextStoreAnchorSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="1ef68-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="1ef68-139">其他架構常數</span><span class="sxs-lookup"><span data-stu-id="1ef68-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





