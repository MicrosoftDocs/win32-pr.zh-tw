---
description: Step 方法會將 DVD-Video 資料流程前移至指定的框架數。
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984656"
---
# <a name="step-method"></a><span data-ttu-id="adee0-103">Step 方法</span><span class="sxs-lookup"><span data-stu-id="adee0-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="adee0-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="adee0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="adee0-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="adee0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="adee0-106">方法會將 `Step` DVD-Video 資料流程前移至指定的框架數。</span><span class="sxs-lookup"><span data-stu-id="adee0-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="adee0-107">參數</span><span class="sxs-lookup"><span data-stu-id="adee0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adee0-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*</span><span class="sxs-lookup"><span data-stu-id="adee0-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="adee0-109">指定要逐步執行為整數的框架數目。</span><span class="sxs-lookup"><span data-stu-id="adee0-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adee0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="adee0-110">Return Value</span></span>

<span data-ttu-id="adee0-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="adee0-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adee0-112">備註</span><span class="sxs-lookup"><span data-stu-id="adee0-112">Remarks</span></span>

<span data-ttu-id="adee0-113">在呼叫這個方法之前，請先呼叫 [**CanStep**](canstep-method.md) 來判斷此解碼器是否支援框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="adee0-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="adee0-114">如果在呼叫這個方法時，DVD-Video 在反向模式下播放，而且此解碼器支援反向框架逐步執行，則會反向執行框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="adee0-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



