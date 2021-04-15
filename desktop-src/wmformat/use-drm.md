---
title: Use_DRM
description: 使用 \_ drm 屬性會指示寫入器物件將 DRM 版本1保護套用至目前的檔案。
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM windows Media 格式
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507784"
---
# <a name="use_drm"></a><span data-ttu-id="ddb3b-104">使用 \_ DRM</span><span class="sxs-lookup"><span data-stu-id="ddb3b-104">Use\_DRM</span></span>

<span data-ttu-id="ddb3b-105">**使用 \_ drm** 屬性會指示寫入器物件將 DRM 版本1保護套用至目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="ddb3b-105">The **Use\_DRM** attribute instructs the writer object to apply DRM version 1 protection to the current file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ddb3b-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="ddb3b-106">Global Constant</span></span>

<span data-ttu-id="ddb3b-107">g \_ wszWMUse \_ DRM</span><span class="sxs-lookup"><span data-stu-id="ddb3b-107">g\_wszWMUse\_DRM</span></span>

## <a name="data-type"></a><span data-ttu-id="ddb3b-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="ddb3b-108">Data Type</span></span>

<span data-ttu-id="ddb3b-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="ddb3b-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb3b-110">備註</span><span class="sxs-lookup"><span data-stu-id="ddb3b-110">Remarks</span></span>

<span data-ttu-id="ddb3b-111">建立 DRM 第1版內容時，請使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ddb3b-111">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property to **TRUE** when creating DRM version 1 content.</span></span> <span data-ttu-id="ddb3b-112">無法從 reader 物件存取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ddb3b-112">This property is not accessible from the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddb3b-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddb3b-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb3b-114">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="ddb3b-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




