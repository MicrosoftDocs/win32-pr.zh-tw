---
description: CanStep 方法會判斷本機系統上的 MPEG-2 解碼器是否可以依照指定的方向執行框架逐步執行。
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: CanStep 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025645"
---
# <a name="canstep-method"></a><span data-ttu-id="12fc6-103">CanStep 方法</span><span class="sxs-lookup"><span data-stu-id="12fc6-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="12fc6-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="12fc6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="12fc6-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="12fc6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="12fc6-106">`CanStep`方法會判斷本機系統上的 mpeg-2 解碼器是否可以依照指定的方向執行框架逐步執行。</span><span class="sxs-lookup"><span data-stu-id="12fc6-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="12fc6-107">參數</span><span class="sxs-lookup"><span data-stu-id="12fc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fc6-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span><span class="sxs-lookup"><span data-stu-id="12fc6-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="12fc6-109">用來作為旗標的布林值，用來指定解碼器的框架逐步執行功能方向、向前或向後。</span><span class="sxs-lookup"><span data-stu-id="12fc6-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="12fc6-110">值</span><span class="sxs-lookup"><span data-stu-id="12fc6-110">Value</span></span> | <span data-ttu-id="12fc6-111">描述</span><span class="sxs-lookup"><span data-stu-id="12fc6-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="12fc6-112">true</span><span class="sxs-lookup"><span data-stu-id="12fc6-112">true</span></span>  | <span data-ttu-id="12fc6-113">是否可以回溯執行解碼器？</span><span class="sxs-lookup"><span data-stu-id="12fc6-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="12fc6-114">false</span><span class="sxs-lookup"><span data-stu-id="12fc6-114">false</span></span> | <span data-ttu-id="12fc6-115">是否可以向前跳到解碼器？</span><span class="sxs-lookup"><span data-stu-id="12fc6-115">Can decoder step forward?</span></span> <span data-ttu-id="12fc6-116">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="12fc6-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fc6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="12fc6-117">Return Value</span></span>

<span data-ttu-id="12fc6-118">如果解碼器可以逐步執行指定的方向，則會傳回布林值 true，否則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="12fc6-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12fc6-119">備註</span><span class="sxs-lookup"><span data-stu-id="12fc6-119">Remarks</span></span>

<span data-ttu-id="12fc6-120">並非所有硬體 MPEG-2 解碼器都支援 DirectShow®8.0 中新的框架逐步執行功能。</span><span class="sxs-lookup"><span data-stu-id="12fc6-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="12fc6-121">這個方法會查詢其框架逐步執行功能的解碼器。</span><span class="sxs-lookup"><span data-stu-id="12fc6-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="12fc6-122">如果此解碼器可以執行畫面格逐步執行，則應用程式可以使用 [**步驟**](step-method.md) 方法來逐步執行畫面格。</span><span class="sxs-lookup"><span data-stu-id="12fc6-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="12fc6-123">如果正在使用軟體解碼器，這個方法一律會傳回 **true** 。</span><span class="sxs-lookup"><span data-stu-id="12fc6-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



