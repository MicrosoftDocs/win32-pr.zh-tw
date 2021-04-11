---
description: 指定 I 與 P 框架之間的連續 B 框架預設數目。
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: 'AVEncMPVDefaultBPictureCount 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025757"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="c00f0-103">AVEncMPVDefaultBPictureCount 屬性</span><span class="sxs-lookup"><span data-stu-id="c00f0-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="c00f0-104">指定 I 與 P 框架之間的連續 B 框架預設數目。</span><span class="sxs-lookup"><span data-stu-id="c00f0-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="c00f0-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c00f0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c00f0-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="c00f0-106">Data type</span></span>

<span data-ttu-id="c00f0-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="c00f0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c00f0-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="c00f0-108">Property GUID</span></span>

<span data-ttu-id="c00f0-109">**CODECAPI \_ AVEncMPVDefaultBPictureCount**</span><span class="sxs-lookup"><span data-stu-id="c00f0-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="c00f0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="c00f0-110">Property value</span></span>

<span data-ttu-id="c00f0-111">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="c00f0-111">This property has a linear range of values.</span></span> <span data-ttu-id="c00f0-112">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="c00f0-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="c00f0-113">備註</span><span class="sxs-lookup"><span data-stu-id="c00f0-113">Remarks</span></span>

<span data-ttu-id="c00f0-114">在 Windows 8 之前，此屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="c00f0-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="c00f0-115">從 Windows 8 開始，MPEG、WMV 和 h.264 影片編碼器會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c00f0-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="c00f0-116">如果編碼器支援這個屬性，它可以用來控制 (GOP) 結構的圖片群組。</span><span class="sxs-lookup"><span data-stu-id="c00f0-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00f0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c00f0-117">Requirements</span></span>



| <span data-ttu-id="c00f0-118">需求</span><span class="sxs-lookup"><span data-stu-id="c00f0-118">Requirement</span></span> | <span data-ttu-id="c00f0-119">值</span><span class="sxs-lookup"><span data-stu-id="c00f0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c00f0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c00f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c00f0-121">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c00f0-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c00f0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c00f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c00f0-123">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c00f0-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c00f0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c00f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00f0-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c00f0-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c00f0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c00f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00f0-127">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="c00f0-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c00f0-128">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="c00f0-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




