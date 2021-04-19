---
title: IsAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986047"
---
# <a name="dvdisavailable"></a><span data-ttu-id="ed952-105">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="ed952-105">DVD.isAvailable</span></span>

<span data-ttu-id="ed952-106">**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="ed952-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="ed952-107">參數</span><span class="sxs-lookup"><span data-stu-id="ed952-107">Parameters</span></span>

<span data-ttu-id="ed952-108">*name*</span><span class="sxs-lookup"><span data-stu-id="ed952-108">*name*</span></span>

<span data-ttu-id="ed952-109">包含下列其中一個值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="ed952-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="ed952-110">String</span><span class="sxs-lookup"><span data-stu-id="ed952-110">String</span></span>     | <span data-ttu-id="ed952-111">Description</span><span class="sxs-lookup"><span data-stu-id="ed952-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed952-112">上一步</span><span class="sxs-lookup"><span data-stu-id="ed952-112">back</span></span>       | <span data-ttu-id="ed952-113">判斷 **back** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="ed952-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="ed952-114">Dvd</span><span class="sxs-lookup"><span data-stu-id="ed952-114">dvd</span></span>        | <span data-ttu-id="ed952-115">判斷是否已載入 DVD。</span><span class="sxs-lookup"><span data-stu-id="ed952-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="ed952-116">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="ed952-116">dvdDecoder</span></span> | <span data-ttu-id="ed952-117">判斷系統上是否已安裝 DVD 解碼器。</span><span class="sxs-lookup"><span data-stu-id="ed952-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="ed952-118">resume</span><span class="sxs-lookup"><span data-stu-id="ed952-118">resume</span></span>     | <span data-ttu-id="ed952-119">判斷 **resume** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="ed952-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="ed952-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="ed952-120">titleMenu</span></span>  | <span data-ttu-id="ed952-121">判斷 **titleMenu** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="ed952-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="ed952-122">topMenu</span><span class="sxs-lookup"><span data-stu-id="ed952-122">topMenu</span></span>    | <span data-ttu-id="ed952-123">判斷 **topMenu** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="ed952-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="ed952-124">通常稱為根功能表。</span><span class="sxs-lookup"><span data-stu-id="ed952-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="ed952-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed952-125">Return Values</span></span>

<span data-ttu-id="ed952-126">這個方法會傳回唯讀的 **布林值** ，指出指定的參數是否可用。</span><span class="sxs-lookup"><span data-stu-id="ed952-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed952-127">備註</span><span class="sxs-lookup"><span data-stu-id="ed952-127">Remarks</span></span>

<span data-ttu-id="ed952-128">Windows Media Player 的 DVD 功能將無法在未安裝協力廠商 DVD 解碼器的電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="ed952-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="ed952-129">您可以藉由呼叫 **isAvailable** ( "dvdDecoder" ) 來判斷是否有可用的解碼器。</span><span class="sxs-lookup"><span data-stu-id="ed952-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="ed952-130">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="ed952-130">Every DVD is authored differently.</span></span> <span data-ttu-id="ed952-131">DVD 播放和流覽期間可用的方法取決於 DVD 的編寫方式。</span><span class="sxs-lookup"><span data-stu-id="ed952-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="ed952-132">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="ed952-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed952-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed952-133">Requirements</span></span>



| <span data-ttu-id="ed952-134">需求</span><span class="sxs-lookup"><span data-stu-id="ed952-134">Requirement</span></span> | <span data-ttu-id="ed952-135">值</span><span class="sxs-lookup"><span data-stu-id="ed952-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed952-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed952-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ed952-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed952-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed952-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed952-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ed952-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed952-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed952-140">版本</span><span class="sxs-lookup"><span data-stu-id="ed952-140">Version</span></span><br/>                  | <span data-ttu-id="ed952-141">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="ed952-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="ed952-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ed952-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed952-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed952-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed952-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed952-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed952-145">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="ed952-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





