---
title: DRM_ActionAllowed_CopyToCD
description: DRM \_ ActionAllowed \_ CopyToCD 屬性會指出是否允許將內容複寫到 CD。
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969091"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="7ca66-104">DRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="7ca66-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="7ca66-105">**DRM \_ ActionAllowed \_ CopyToCD** 屬性會指出是否允許將內容複寫到 CD。</span><span class="sxs-lookup"><span data-stu-id="7ca66-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7ca66-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="7ca66-106">Global Constant</span></span>

<span data-ttu-id="7ca66-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="7ca66-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="7ca66-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="7ca66-108">Data Type</span></span>

<span data-ttu-id="7ca66-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="7ca66-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca66-110">備註</span><span class="sxs-lookup"><span data-stu-id="7ca66-110">Remarks</span></span>

<span data-ttu-id="7ca66-111">Windows Media DRM 10 授權使用複製動作來限制複製到 CD。</span><span class="sxs-lookup"><span data-stu-id="7ca66-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="7ca66-112">您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。</span><span class="sxs-lookup"><span data-stu-id="7ca66-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="7ca66-113">這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="7ca66-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="7ca66-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ca66-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca66-115">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="7ca66-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




