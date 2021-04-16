---
description: 指定媒體範例是否為數據流中間距之後的第一個範例。
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: 'MFSampleExtension_Discontinuity 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512624"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="a5818-103">MFSampleExtension 不連續 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="a5818-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="a5818-104">指定媒體範例是否為數據流中間距之後的第一個範例。</span><span class="sxs-lookup"><span data-stu-id="a5818-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5818-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a5818-105">Data type</span></span>

<span data-ttu-id="a5818-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5818-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a5818-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="a5818-107">Get/set</span></span>

<span data-ttu-id="a5818-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="a5818-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a5818-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="a5818-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a5818-110">適用於</span><span class="sxs-lookup"><span data-stu-id="a5818-110">Applies to</span></span>

[<span data-ttu-id="a5818-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="a5818-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="a5818-112">備註</span><span class="sxs-lookup"><span data-stu-id="a5818-112">Remarks</span></span>

<span data-ttu-id="a5818-113">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="a5818-113">This attribute applies to media samples.</span></span> <span data-ttu-id="a5818-114">如果此屬性為 **TRUE**，則表示資料流程中發生不連續的情況，而且此範例是在間距之後出現的第一個。</span><span class="sxs-lookup"><span data-stu-id="a5818-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="a5818-115">如果未設定此屬性，則預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a5818-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="a5818-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a5818-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5818-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5818-117">Requirements</span></span>



| <span data-ttu-id="a5818-118">需求</span><span class="sxs-lookup"><span data-stu-id="a5818-118">Requirement</span></span> | <span data-ttu-id="a5818-119">值</span><span class="sxs-lookup"><span data-stu-id="a5818-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5818-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5818-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5818-121">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5818-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a5818-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5818-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5818-123">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5818-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a5818-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a5818-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5818-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5818-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5818-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5818-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5818-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a5818-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5818-128">範例屬性</span><span class="sxs-lookup"><span data-stu-id="a5818-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5818-129">媒體範例</span><span class="sxs-lookup"><span data-stu-id="a5818-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




