---
title: DRM_DRMHeader_SubscriptionContentID
description: DRM \_ DRMHeader \_ SubscriptionContentID 屬性包含訂用帳戶內容識別碼。
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932928"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="4286b-104">DRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="4286b-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="4286b-105">**DRM \_ DRMHeader \_ SubscriptionContentID** 屬性包含訂用帳戶內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="4286b-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4286b-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="4286b-106">Global Constant</span></span>

<span data-ttu-id="4286b-107">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="4286b-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="4286b-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="4286b-108">Data Type</span></span>

<span data-ttu-id="4286b-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="4286b-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="4286b-110">備註</span><span class="sxs-lookup"><span data-stu-id="4286b-110">Remarks</span></span>

<span data-ttu-id="4286b-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="4286b-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="4286b-112">訂用帳戶內容識別碼是選擇性的，只由內容建立者決定。</span><span class="sxs-lookup"><span data-stu-id="4286b-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="4286b-113">寫入器物件不會對此屬性執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="4286b-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="4286b-114">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。</span><span class="sxs-lookup"><span data-stu-id="4286b-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="4286b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4286b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4286b-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="4286b-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




