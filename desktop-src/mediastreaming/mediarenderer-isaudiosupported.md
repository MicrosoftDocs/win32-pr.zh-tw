---
title: MediaRenderer. IsAudioSupported 屬性
description: 取得值，這個值會指出 DMR 是否能夠播放音訊內容。
ms.assetid: a1965cba-3e7c-4a81-ab1d-6d3af7826115
keywords:
- IsAudioSupported 屬性媒體串流 API
- IsAudioSupported 屬性媒體串流 API，MediaRenderer 介面
- MediaRenderer 介面媒體串流 API，IsAudioSupported 屬性
topic_type:
- apiref
api_name:
- MediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e948e3c7b3a1c00c7a3fb5fe6a758849f060545a
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313268"
---
# <a name="mediarendererisaudiosupported-property"></a><span data-ttu-id="1a3c3-106">MediaRenderer. IsAudioSupported 屬性</span><span class="sxs-lookup"><span data-stu-id="1a3c3-106">MediaRenderer.IsAudioSupported property</span></span>

<span data-ttu-id="1a3c3-107">取得值，這個值會指出 DMR 是否能夠播放音訊內容。</span><span class="sxs-lookup"><span data-stu-id="1a3c3-107">Gets a value that indicates whether the DMR is capable of playing audio content.</span></span>

<span data-ttu-id="1a3c3-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1a3c3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3c3-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a3c3-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="1a3c3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1a3c3-110">Property value</span></span>

<span data-ttu-id="1a3c3-111">布林值，如果 DMR 能夠播放音訊內容，則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="1a3c3-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a3c3-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a3c3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3c3-113">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="1a3c3-113">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 




