---
title: DRM_LicenseID
description: DRM \_ LicenseID 屬性包含從與目前開啟的檔案（可唯一識別該授權）相關聯的授權中取出的字串。
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314346"
---
# <a name="drm_licenseid"></a><span data-ttu-id="fc528-104">DRM \_ LicenseID</span><span class="sxs-lookup"><span data-stu-id="fc528-104">DRM\_LicenseID</span></span>

<span data-ttu-id="fc528-105">**DRM \_ LicenseID** 屬性包含從與目前開啟的檔案（可唯一識別該授權）相關聯的授權中取出的字串。</span><span class="sxs-lookup"><span data-stu-id="fc528-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fc528-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="fc528-106">Global Constant</span></span>

<span data-ttu-id="fc528-107">g \_ wszWMDRM \_ LicenseID</span><span class="sxs-lookup"><span data-stu-id="fc528-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="fc528-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fc528-108">Data Type</span></span>

<span data-ttu-id="fc528-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="fc528-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc528-110">備註</span><span class="sxs-lookup"><span data-stu-id="fc528-110">Remarks</span></span>

<span data-ttu-id="fc528-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="fc528-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="fc528-112">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。</span><span class="sxs-lookup"><span data-stu-id="fc528-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="fc528-113">授權識別碼會儲存在授權中，而不是儲存在 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="fc528-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="fc528-114">每個個別授權都有唯一的識別碼，由授權產生器在建立授權時指派。</span><span class="sxs-lookup"><span data-stu-id="fc528-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="fc528-115">例如，如果您取得相同內容的兩個授權，每一個授權都會有不同的 LicenseID 屬性。</span><span class="sxs-lookup"><span data-stu-id="fc528-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="fc528-116">一般來說，應用程式不需要取得此值。</span><span class="sxs-lookup"><span data-stu-id="fc528-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc528-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc528-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc528-118">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="fc528-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




