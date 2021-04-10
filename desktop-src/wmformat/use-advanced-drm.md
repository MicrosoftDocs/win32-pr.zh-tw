---
title: Use_Advanced_DRM
description: '[使用 \_ Advanced \_ drm] 屬性會指定是否使用 DRM 第7版來保護內容。'
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM windows Media 格式
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8720d5b401a1a1cec5240920bfb4a3811012420
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104185468"
---
# <a name="use_advanced_drm"></a><span data-ttu-id="d06b7-104">使用 \_ Advanced \_ DRM</span><span class="sxs-lookup"><span data-stu-id="d06b7-104">Use\_Advanced\_DRM</span></span>

<span data-ttu-id="d06b7-105">[ **使用 \_ Advanced \_ drm** ] 屬性會指定是否使用 DRM 第7版來保護內容。</span><span class="sxs-lookup"><span data-stu-id="d06b7-105">The **Use\_Advanced\_DRM** attribute specifies whether DRM version 7 is used to protect the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d06b7-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="d06b7-106">Global Constant</span></span>

<span data-ttu-id="d06b7-107">g \_ wszWMUse \_ Advanced \_ DRM</span><span class="sxs-lookup"><span data-stu-id="d06b7-107">g\_wszWMUse\_Advanced\_DRM</span></span>

## <a name="data-type"></a><span data-ttu-id="d06b7-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="d06b7-108">Data Type</span></span>

<span data-ttu-id="d06b7-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="d06b7-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="d06b7-110">備註</span><span class="sxs-lookup"><span data-stu-id="d06b7-110">Remarks</span></span>

<span data-ttu-id="d06b7-111">這是讀寫屬性，會使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) 抓取，並使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)進行設定。</span><span class="sxs-lookup"><span data-stu-id="d06b7-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="d06b7-112">無法從 reader 物件存取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d06b7-112">This property is not accessible from the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="d06b7-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d06b7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06b7-114">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="d06b7-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




