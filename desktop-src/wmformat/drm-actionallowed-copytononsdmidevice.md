---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: DRM \_ ActionAllowed \_ CopyToNonSDMIDevice 屬性會指出是否允許將內容複寫到非 SDMI 裝置。
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023070"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="cdd47-104">DRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="cdd47-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="cdd47-105">**DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** 屬性會指出是否允許將內容複寫到非 SDMI 裝置</span><span class="sxs-lookup"><span data-stu-id="cdd47-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="cdd47-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="cdd47-106">Global Constant</span></span>

<span data-ttu-id="cdd47-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="cdd47-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="cdd47-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="cdd47-108">Data Type</span></span>

<span data-ttu-id="cdd47-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="cdd47-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd47-110">備註</span><span class="sxs-lookup"><span data-stu-id="cdd47-110">Remarks</span></span>

<span data-ttu-id="cdd47-111">Windows Media DRM 10 授權使用複製動作來限制複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="cdd47-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="cdd47-112">您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。</span><span class="sxs-lookup"><span data-stu-id="cdd47-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="cdd47-113">這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="cdd47-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="cdd47-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd47-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd47-115">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="cdd47-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




