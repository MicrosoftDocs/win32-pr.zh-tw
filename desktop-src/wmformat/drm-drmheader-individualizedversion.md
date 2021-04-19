---
title: DRM_DRMHeader_IndividualizedVersion
description: DRM \_ DRMHeaderIndividualizedVersion 屬性包含播放檔案所需的最小個別版本。
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966230"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="2a665-104">DRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="2a665-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="2a665-105">**DRM \_ DRMHeaderIndividualizedVersion** 屬性包含播放檔案所需的最小個別版本。</span><span class="sxs-lookup"><span data-stu-id="2a665-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2a665-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="2a665-106">Global Constant</span></span>

<span data-ttu-id="2a665-107">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="2a665-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="2a665-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="2a665-108">Data Type</span></span>

<span data-ttu-id="2a665-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="2a665-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a665-110">備註</span><span class="sxs-lookup"><span data-stu-id="2a665-110">Remarks</span></span>

<span data-ttu-id="2a665-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="2a665-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="2a665-112">您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。</span><span class="sxs-lookup"><span data-stu-id="2a665-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="2a665-113">若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 在檔案上設定個別的版本 (也稱為安全性版本) ，您必須使用 [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2a665-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a665-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a665-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a665-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="2a665-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




