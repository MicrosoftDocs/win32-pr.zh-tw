---
description: 指定交錯式影片框架的欄位支配。
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: 'MFSampleExtension_BottomFieldFirst 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318923"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="3c937-103">MFSampleExtension \_ BottomFieldFirst 屬性</span><span class="sxs-lookup"><span data-stu-id="3c937-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="3c937-104">指定交錯式影片框架的欄位支配。</span><span class="sxs-lookup"><span data-stu-id="3c937-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="3c937-105">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3c937-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c937-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="3c937-106">Data type</span></span>

<span data-ttu-id="3c937-107">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c937-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3c937-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3c937-108">Get/set</span></span>

<span data-ttu-id="3c937-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="3c937-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3c937-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="3c937-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3c937-111">適用於</span><span class="sxs-lookup"><span data-stu-id="3c937-111">Applies to</span></span>

[<span data-ttu-id="3c937-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="3c937-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="3c937-113">備註</span><span class="sxs-lookup"><span data-stu-id="3c937-113">Remarks</span></span>

<span data-ttu-id="3c937-114">如果影片框架是交錯的，且此範例包含兩個交錯的欄位，這個屬性會指出先顯示哪個欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="3c937-115">若 **為 TRUE**，則底部欄位為第一個時間。</span><span class="sxs-lookup"><span data-stu-id="3c937-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="3c937-116">如果 **為 FALSE**，則表示頂端欄位是 first。</span><span class="sxs-lookup"><span data-stu-id="3c937-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="3c937-117">如果框架是交錯的，且範例包含單一欄位，則此屬性會指出此範例包含的欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="3c937-118">若 **為 TRUE**，則範例包含底部欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="3c937-119">如果 **為 FALSE**，則表示範例包含上方欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="3c937-120">如果框架是漸進式的，則此屬性會描述在輸出交錯時如何排序欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="3c937-121">若 **為 TRUE**，則應先輸出下一個欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="3c937-122">如果 **為 FALSE**，則應該先輸出最上層欄位。</span><span class="sxs-lookup"><span data-stu-id="3c937-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="3c937-123">如果未設定此屬性，則媒體類型會描述欄位支配。</span><span class="sxs-lookup"><span data-stu-id="3c937-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="3c937-124">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3c937-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c937-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c937-125">Requirements</span></span>



| <span data-ttu-id="3c937-126">需求</span><span class="sxs-lookup"><span data-stu-id="3c937-126">Requirement</span></span> | <span data-ttu-id="3c937-127">值</span><span class="sxs-lookup"><span data-stu-id="3c937-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c937-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c937-129">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c937-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3c937-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c937-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c937-131">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c937-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3c937-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3c937-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c937-133"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c937-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c937-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c937-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c937-135">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3c937-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c937-136">範例屬性</span><span class="sxs-lookup"><span data-stu-id="3c937-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c937-137">媒體範例</span><span class="sxs-lookup"><span data-stu-id="3c937-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="3c937-138">影片交錯</span><span class="sxs-lookup"><span data-stu-id="3c937-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




