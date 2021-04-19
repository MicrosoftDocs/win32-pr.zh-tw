---
title: 設定. isAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |設定. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- 設定. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992895"
---
# <a name="settingsisavailable"></a><span data-ttu-id="11bb9-105">設定. isAvailable</span><span class="sxs-lookup"><span data-stu-id="11bb9-105">Settings.isAvailable</span></span>

<span data-ttu-id="11bb9-106">**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="11bb9-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bb9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11bb9-107">Syntax</span></span>

<span data-ttu-id="11bb9-108">isAvailable ( 名稱 ) </span><span class="sxs-lookup"><span data-stu-id="11bb9-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="11bb9-109">參數</span><span class="sxs-lookup"><span data-stu-id="11bb9-109">Parameters</span></span>

<span data-ttu-id="11bb9-110">*name*</span><span class="sxs-lookup"><span data-stu-id="11bb9-110">*name*</span></span>

<span data-ttu-id="11bb9-111">包含下列其中一個值的字串。</span><span class="sxs-lookup"><span data-stu-id="11bb9-111">String containing one of the following values.</span></span>



| <span data-ttu-id="11bb9-112">String</span><span class="sxs-lookup"><span data-stu-id="11bb9-112">String</span></span>             | <span data-ttu-id="11bb9-113">Description</span><span class="sxs-lookup"><span data-stu-id="11bb9-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="11bb9-114">AutoStart</span><span class="sxs-lookup"><span data-stu-id="11bb9-114">AutoStart</span></span>          | <span data-ttu-id="11bb9-115">判斷是否可以設定自動啟動屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="11bb9-116">餘額</span><span class="sxs-lookup"><span data-stu-id="11bb9-116">Balance</span></span>            | <span data-ttu-id="11bb9-117">決定是否可以設定餘額屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="11bb9-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="11bb9-118">BaseURL</span></span>            | <span data-ttu-id="11bb9-119">判斷是否可以設定 baseURL 屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="11bb9-120">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="11bb9-120">DefaultFrame</span></span>       | <span data-ttu-id="11bb9-121">判斷是否可以設定 defaultFrame 屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="11bb9-122">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="11bb9-122">EnableErrorDialogs</span></span> | <span data-ttu-id="11bb9-123">判斷是否可以設定 enableErrorDialogs 屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="11bb9-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="11bb9-124">GetMode</span></span>            | <span data-ttu-id="11bb9-125">判斷是否可以呼叫 getMode 方法。</span><span class="sxs-lookup"><span data-stu-id="11bb9-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="11bb9-126">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="11bb9-126">InvokeURLs</span></span>         | <span data-ttu-id="11bb9-127">判斷是否可以設定 invokeURLs 屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="11bb9-128">Mute</span><span class="sxs-lookup"><span data-stu-id="11bb9-128">Mute</span></span>               | <span data-ttu-id="11bb9-129">決定是否可以設定靜音屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="11bb9-130">PlayCount</span><span class="sxs-lookup"><span data-stu-id="11bb9-130">PlayCount</span></span>          | <span data-ttu-id="11bb9-131">判斷是否可以設定 playCount 屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="11bb9-132">費率</span><span class="sxs-lookup"><span data-stu-id="11bb9-132">Rate</span></span>               | <span data-ttu-id="11bb9-133">決定是否可以設定速率屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="11bb9-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="11bb9-134">SetMode</span></span>            | <span data-ttu-id="11bb9-135">判斷是否可以呼叫 setMode 方法。</span><span class="sxs-lookup"><span data-stu-id="11bb9-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="11bb9-136">磁碟區</span><span class="sxs-lookup"><span data-stu-id="11bb9-136">Volume</span></span>             | <span data-ttu-id="11bb9-137">判斷是否可以設定磁片區屬性。</span><span class="sxs-lookup"><span data-stu-id="11bb9-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="11bb9-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="11bb9-138">Return Values</span></span>

<span data-ttu-id="11bb9-139">這個方法會傳回 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="11bb9-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bb9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="11bb9-140">Requirements</span></span>



| <span data-ttu-id="11bb9-141">需求</span><span class="sxs-lookup"><span data-stu-id="11bb9-141">Requirement</span></span> | <span data-ttu-id="11bb9-142">值</span><span class="sxs-lookup"><span data-stu-id="11bb9-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11bb9-143">版本</span><span class="sxs-lookup"><span data-stu-id="11bb9-143">Version</span></span><br/> | <span data-ttu-id="11bb9-144">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="11bb9-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="11bb9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="11bb9-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="11bb9-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11bb9-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11bb9-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11bb9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bb9-148">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="11bb9-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





