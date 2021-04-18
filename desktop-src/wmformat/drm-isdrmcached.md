---
title: DRM_IsDRMCached
description: DRM \_ IsDRMCached 屬性會指出是否已在本機電腦上儲存 drm 版本1授權資訊。
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached windows Media 格式
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965832"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="557d5-104">DRM \_ IsDRMCached</span><span class="sxs-lookup"><span data-stu-id="557d5-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="557d5-105">**Drm \_ IsDRMCached** 屬性會指出是否已在本機電腦上儲存 drm 版本1授權資訊。</span><span class="sxs-lookup"><span data-stu-id="557d5-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="557d5-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="557d5-106">Global Constant</span></span>

<span data-ttu-id="557d5-107">g \_ wszWMDRM \_ IsDRMCached</span><span class="sxs-lookup"><span data-stu-id="557d5-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="557d5-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="557d5-108">Data Type</span></span>

<span data-ttu-id="557d5-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="557d5-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="557d5-110">備註</span><span class="sxs-lookup"><span data-stu-id="557d5-110">Remarks</span></span>

<span data-ttu-id="557d5-111">這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="557d5-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="557d5-112">當授權取得 URL 符合在 DRM 第1版中用來取得本機授權的兩個已知 Url 之一時，即為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="557d5-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="557d5-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="557d5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557d5-114">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="557d5-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




