---
description: 取得已解碼影像的大小（以圖元為單位）。
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: 'AVDecVideoImageSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972750"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="e4321-103">AVDecVideoImageSize 屬性</span><span class="sxs-lookup"><span data-stu-id="e4321-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="e4321-104">取得已解碼影像的大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4321-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="e4321-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4321-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4321-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="e4321-106">Data type</span></span>

<span data-ttu-id="e4321-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="e4321-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e4321-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="e4321-108">Property GUID</span></span>

<span data-ttu-id="e4321-109">**CODECAPI \_ AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="e4321-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="e4321-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4321-110">Property value</span></span>

<span data-ttu-id="e4321-111">高16位包含寬度，而低16位則包含高度。</span><span class="sxs-lookup"><span data-stu-id="e4321-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4321-112">備註</span><span class="sxs-lookup"><span data-stu-id="e4321-112">Remarks</span></span>

<span data-ttu-id="e4321-113">通道數目包含 (LFE) 通道的低頻率效果（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e4321-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4321-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4321-114">Requirements</span></span>



| <span data-ttu-id="e4321-115">需求</span><span class="sxs-lookup"><span data-stu-id="e4321-115">Requirement</span></span> | <span data-ttu-id="e4321-116">值</span><span class="sxs-lookup"><span data-stu-id="e4321-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4321-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4321-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4321-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4321-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e4321-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4321-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4321-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4321-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e4321-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e4321-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4321-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4321-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4321-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4321-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4321-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="e4321-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e4321-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="e4321-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




