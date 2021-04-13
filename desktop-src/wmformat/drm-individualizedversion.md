---
title: DRM_IndividualizedVersion
description: DRM \_ IndividualizedVersion 屬性會儲存在 drm 標頭中，並包含存取內容所需的最小個別版本。
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion windows Media 格式
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314358"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="e5275-104">DRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="e5275-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="e5275-105">**Drm \_ IndividualizedVersion** 屬性會儲存在 drm 標頭中，並包含存取內容所需的最小個別版本。</span><span class="sxs-lookup"><span data-stu-id="e5275-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e5275-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="e5275-106">Global Constant</span></span>

<span data-ttu-id="e5275-107">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="e5275-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="e5275-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="e5275-108">Data Type</span></span>

<span data-ttu-id="e5275-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="e5275-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="e5275-110">備註</span><span class="sxs-lookup"><span data-stu-id="e5275-110">Remarks</span></span>

<span data-ttu-id="e5275-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="e5275-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="e5275-112">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。</span><span class="sxs-lookup"><span data-stu-id="e5275-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="e5275-113">您可以使用 [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md)來取出相同的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="e5275-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e5275-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5275-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5275-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="e5275-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




