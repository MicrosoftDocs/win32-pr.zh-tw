---
title: DRM_BaseLicenseAcqURL
description: DRM \_ BaseLicenseAcqURL 屬性包含部分的基底 URL，播放程式應用程式必須流覽此 URL 才能取得內容的授權。
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL windows Media 格式
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092534"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="d1b77-104">DRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d1b77-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="d1b77-105">**DRM \_ BaseLicenseAcqURL** 屬性包含部分的基底 URL，播放程式應用程式必須流覽此 URL 才能取得內容的授權。</span><span class="sxs-lookup"><span data-stu-id="d1b77-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d1b77-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="d1b77-106">Global Constant</span></span>

<span data-ttu-id="d1b77-107">g \_ wszWMDRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d1b77-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="d1b77-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="d1b77-108">Data Type</span></span>

<span data-ttu-id="d1b77-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="d1b77-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b77-110">備註</span><span class="sxs-lookup"><span data-stu-id="d1b77-110">Remarks</span></span>

<span data-ttu-id="d1b77-111">這是選擇性的讀寫屬性，它是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)設定和取出。</span><span class="sxs-lookup"><span data-stu-id="d1b77-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d1b77-112">提供此功能的目的是讓授權散發系統在授權取得 URL 屬性中使用相對路徑。</span><span class="sxs-lookup"><span data-stu-id="d1b77-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="d1b77-113">設定這個屬性之後，內容標頭中的所有部分授權取得 Url 都會將基底 URL 新增至部分 URL 的前方，以構成播放程式要流覽的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="d1b77-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="d1b77-114">針對 **DRM \_ BaseLicenseAcqURL** 呼叫 **IWMDRMReader：： GetDRMProperty** 只會在設定的相同會話中運作。</span><span class="sxs-lookup"><span data-stu-id="d1b77-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="d1b77-115">屬性不會儲存在內容標頭中;它是動態的，且只有相對 URL 會儲存在內容中。</span><span class="sxs-lookup"><span data-stu-id="d1b77-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1b77-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1b77-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b77-117">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="d1b77-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




