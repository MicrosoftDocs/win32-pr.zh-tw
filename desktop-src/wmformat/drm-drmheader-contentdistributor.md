---
title: DRM_DRMHeader_ContentDistributor
description: DRM \_ DRMHeader \_ ContentDistributor 屬性包含 identifiying 內容散發者的字串。
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966843"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="3ab59-104">DRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="3ab59-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="3ab59-105">**DRM \_ DRMHeader \_ ContentDistributor** 屬性包含 identifiying 內容散發者的字串。</span><span class="sxs-lookup"><span data-stu-id="3ab59-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3ab59-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="3ab59-106">Global Constant</span></span>

<span data-ttu-id="3ab59-107">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="3ab59-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="3ab59-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="3ab59-108">Data Type</span></span>

<span data-ttu-id="3ab59-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="3ab59-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3ab59-110">備註</span><span class="sxs-lookup"><span data-stu-id="3ab59-110">Remarks</span></span>

<span data-ttu-id="3ab59-111">內容識別碼是選擇性的，只由內容建立者決定。</span><span class="sxs-lookup"><span data-stu-id="3ab59-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="3ab59-112">寫入器物件不會對此屬性執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="3ab59-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="3ab59-113">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="3ab59-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="3ab59-114">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。</span><span class="sxs-lookup"><span data-stu-id="3ab59-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ab59-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ab59-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab59-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="3ab59-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




