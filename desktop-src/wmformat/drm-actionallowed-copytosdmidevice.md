---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: DRM \_ ActionAllowed \_ CopyToSDMIDevice 屬性會指出是否允許將內容複寫到 SDMI 裝置。
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374347"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="dc47a-104">DRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="dc47a-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="dc47a-105">**DRM \_ ActionAllowed \_ CopyToSDMIDevice** 屬性會指出是否允許將內容複寫到 SDMI 裝置。</span><span class="sxs-lookup"><span data-stu-id="dc47a-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="dc47a-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="dc47a-106">Global Constant</span></span>

<span data-ttu-id="dc47a-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="dc47a-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="dc47a-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="dc47a-108">Data Type</span></span>

<span data-ttu-id="dc47a-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="dc47a-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc47a-110">備註</span><span class="sxs-lookup"><span data-stu-id="dc47a-110">Remarks</span></span>

<span data-ttu-id="dc47a-111">Windows Media DRM 10 授權使用複製動作來限制複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="dc47a-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="dc47a-112">您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。</span><span class="sxs-lookup"><span data-stu-id="dc47a-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="dc47a-113">這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="dc47a-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="dc47a-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc47a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc47a-115">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="dc47a-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




