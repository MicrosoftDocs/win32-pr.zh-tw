---
title: 'IWMPDVD. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法會取得值，這個值表示指定的資訊類型是否可用或是否可以執行指定的動作。
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999640"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="c558b-104">IWMPDVD. isAvailable (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="c558b-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="c558b-105">**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="c558b-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="c558b-106">參數</span><span class="sxs-lookup"><span data-stu-id="c558b-106">Parameters</span></span>

<span data-ttu-id="c558b-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="c558b-107">*bstrItem*</span></span>

<span data-ttu-id="c558b-108">System.string，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c558b-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="c558b-109">值</span><span class="sxs-lookup"><span data-stu-id="c558b-109">Value</span></span>      | <span data-ttu-id="c558b-110">描述</span><span class="sxs-lookup"><span data-stu-id="c558b-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c558b-111">上一步</span><span class="sxs-lookup"><span data-stu-id="c558b-111">back</span></span>       | <span data-ttu-id="c558b-112">探索 **IWMPDVD** 的方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="c558b-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="c558b-113">Dvd</span><span class="sxs-lookup"><span data-stu-id="c558b-113">dvd</span></span>        | <span data-ttu-id="c558b-114">探索是否已載入 DVD。</span><span class="sxs-lookup"><span data-stu-id="c558b-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="c558b-115">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="c558b-115">dvdDecoder</span></span> | <span data-ttu-id="c558b-116">探索系統上是否已安裝 DVD 解碼器。</span><span class="sxs-lookup"><span data-stu-id="c558b-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="c558b-117">resume</span><span class="sxs-lookup"><span data-stu-id="c558b-117">resume</span></span>     | <span data-ttu-id="c558b-118">探索 IWMPDVD 的 **resume** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="c558b-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="c558b-119">titleMenu</span><span class="sxs-lookup"><span data-stu-id="c558b-119">titleMenu</span></span>  | <span data-ttu-id="c558b-120">探索 **IWMPDVD. titleMenu** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="c558b-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="c558b-121">topMenu</span><span class="sxs-lookup"><span data-stu-id="c558b-121">topMenu</span></span>    | <span data-ttu-id="c558b-122">探索 **IWMPDVD. topMenu** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="c558b-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="c558b-123">通常稱為根功能表。</span><span class="sxs-lookup"><span data-stu-id="c558b-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="c558b-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="c558b-124">Property Value</span></span>

<span data-ttu-id="c558b-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="c558b-125">**System.Boolean**</span></span>

<span data-ttu-id="c558b-126">**布林值**，指出指定的資訊類型是否可用，或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="c558b-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c558b-127">備註</span><span class="sxs-lookup"><span data-stu-id="c558b-127">Remarks</span></span>

<span data-ttu-id="c558b-128">Windows Media Player 的 DVD 功能將無法在未安裝 DVD 解碼器的電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="c558b-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="c558b-129">您可以在 c ) # 中呼叫 **isAvailable** 屬性 (**get \_ isAvailable** 方法，並傳入 **system.string** 值 "dvdDecoder" 來判斷是否有可用的解碼器。</span><span class="sxs-lookup"><span data-stu-id="c558b-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="c558b-130">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="c558b-130">Every DVD is authored differently.</span></span> <span data-ttu-id="c558b-131">DVD 播放和流覽期間可用的方法取決於 DVD 的編寫方式。</span><span class="sxs-lookup"><span data-stu-id="c558b-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c558b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c558b-132">Requirements</span></span>



| <span data-ttu-id="c558b-133">需求</span><span class="sxs-lookup"><span data-stu-id="c558b-133">Requirement</span></span> | <span data-ttu-id="c558b-134">值</span><span class="sxs-lookup"><span data-stu-id="c558b-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c558b-135">版本</span><span class="sxs-lookup"><span data-stu-id="c558b-135">Version</span></span><br/>   | <span data-ttu-id="c558b-136">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="c558b-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c558b-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="c558b-137">Namespace</span></span><br/> | <span data-ttu-id="c558b-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c558b-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c558b-139">組件</span><span class="sxs-lookup"><span data-stu-id="c558b-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c558b-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c558b-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c558b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c558b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c558b-142">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c558b-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c558b-143">**IWMPDVD. back (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c558b-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c558b-144">**IWMPDVD 繼續 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c558b-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c558b-145">**IWMPDVD. titleMenu (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c558b-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c558b-146">**IWMPDVD. topMenu (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c558b-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





