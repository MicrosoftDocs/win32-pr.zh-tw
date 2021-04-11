---
title: BasicDevice 圖示屬性
description: 取得 IDeviceIcon 介面的向量。
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- 圖示屬性媒體串流 API
- 圖示屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，圖示屬性
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375257"
---
# <a name="basicdeviceicons-property"></a><span data-ttu-id="9d61e-106">BasicDevice 圖示屬性</span><span class="sxs-lookup"><span data-stu-id="9d61e-106">BasicDevice.Icons property</span></span>

<span data-ttu-id="9d61e-107">取得 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。</span><span class="sxs-lookup"><span data-stu-id="9d61e-107">Gets a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

<span data-ttu-id="9d61e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9d61e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d61e-109">語法</span><span class="sxs-lookup"><span data-stu-id="9d61e-109">Syntax</span></span>


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a><span data-ttu-id="9d61e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9d61e-110">Property value</span></span>

<span data-ttu-id="9d61e-111">[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)介面指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="9d61e-111">An enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d61e-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d61e-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d61e-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d61e-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

 