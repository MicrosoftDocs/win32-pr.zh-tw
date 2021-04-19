---
title: ServiceTask1 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ServiceTask1 元素代表第一個線上商店工作窗格。
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- ServiceTask1 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993348"
---
# <a name="servicetask1-element"></a><span data-ttu-id="2abdd-106">ServiceTask1 元素</span><span class="sxs-lookup"><span data-stu-id="2abdd-106">ServiceTask1 Element</span></span>

> [!Note]  
> <span data-ttu-id="2abdd-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="2abdd-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2abdd-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2abdd-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2abdd-109">**ServiceTask1** 元素代表第一個線上商店工作窗格。</span><span class="sxs-lookup"><span data-stu-id="2abdd-109">The **ServiceTask1** element represents the first online store task pane.</span></span>

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="2abdd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2abdd-110">Attributes</span></span>



| <span data-ttu-id="2abdd-111">詞彙</span><span class="sxs-lookup"><span data-stu-id="2abdd-111">Term</span></span>                                                                                                                             | <span data-ttu-id="2abdd-112">描述</span><span class="sxs-lookup"><span data-stu-id="2abdd-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2abdd-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) </span><span class="sxs-lookup"><span data-stu-id="2abdd-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="2abdd-114">Windows Media Player 顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="2abdd-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="2abdd-115">父/子項目</span><span class="sxs-lookup"><span data-stu-id="2abdd-115">Parent/Child Elements</span></span>



| <span data-ttu-id="2abdd-116">階層</span><span class="sxs-lookup"><span data-stu-id="2abdd-116">Hierarchy</span></span>       | <span data-ttu-id="2abdd-117">元素</span><span class="sxs-lookup"><span data-stu-id="2abdd-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="2abdd-118">父元素</span><span class="sxs-lookup"><span data-stu-id="2abdd-118">Parent elements</span></span> | <span data-ttu-id="2abdd-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="2abdd-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="2abdd-120">子元素</span><span class="sxs-lookup"><span data-stu-id="2abdd-120">Child elements</span></span>  | <span data-ttu-id="2abdd-121">**ButtonText**、 **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="2abdd-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2abdd-122">備註</span><span class="sxs-lookup"><span data-stu-id="2abdd-122">Remarks</span></span>

<span data-ttu-id="2abdd-123">**ServiceTask1** 被視為參與商務工作的主要工作窗格。</span><span class="sxs-lookup"><span data-stu-id="2abdd-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="2abdd-124">它是使用者選擇購買音樂時所顯示的工作窗格。</span><span class="sxs-lookup"><span data-stu-id="2abdd-124">It is the task pane that displays when the user chooses to purchase music.</span></span>

> [!Note]  
> <span data-ttu-id="2abdd-125">Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。</span><span class="sxs-lookup"><span data-stu-id="2abdd-125">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="2abdd-126">線上商店可以選擇使用一個、兩個或三個工作窗格。</span><span class="sxs-lookup"><span data-stu-id="2abdd-126">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="2abdd-127">Windows Media Player 11 只有一個工作窗格（以 **ServiceTask1** 表示），使用者可以按一下 [ **線上商店** ] 索引標籤來加以查看。</span><span class="sxs-lookup"><span data-stu-id="2abdd-127">Windows Media Player 11 has only one task pane, represented by **ServiceTask1**, which the user can view by clicking on the **Online Stores** tab.</span></span>

 

<span data-ttu-id="2abdd-128">線上商店工作窗格共用單一瀏覽器實例。</span><span class="sxs-lookup"><span data-stu-id="2abdd-128">Online store task panes share a single browser instance.</span></span> <span data-ttu-id="2abdd-129">這表示當使用者切換離開目前的服務工作時，您不應該在網頁中撰寫預期會繼續執行的腳本程式碼。</span><span class="sxs-lookup"><span data-stu-id="2abdd-129">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="2abdd-130">當使用者切換工作窗格時，Windows Media Player 會儲存 URL 和會話 cookie。</span><span class="sxs-lookup"><span data-stu-id="2abdd-130">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="2abdd-131">當使用者切換回工作窗格時，播放玩家會還原 URL 和 cookie。</span><span class="sxs-lookup"><span data-stu-id="2abdd-131">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="2abdd-132">如果使用者選擇使用不同的線上商店，則會清除 URL 和會話資料。</span><span class="sxs-lookup"><span data-stu-id="2abdd-132">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="2abdd-133">下表詳細說明以 URL 要求傳送的參數。</span><span class="sxs-lookup"><span data-stu-id="2abdd-133">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="2abdd-134">其他可能存在於舊版相容性的用途。</span><span class="sxs-lookup"><span data-stu-id="2abdd-134">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="2abdd-135">Name</span><span class="sxs-lookup"><span data-stu-id="2abdd-135">Name</span></span>         | <span data-ttu-id="2abdd-136">值</span><span class="sxs-lookup"><span data-stu-id="2abdd-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abdd-137">*大地 水準面*</span><span class="sxs-lookup"><span data-stu-id="2abdd-137">*geoid*</span></span>      | <span data-ttu-id="2abdd-138">Windows 地理位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2abdd-138">Windows geographical location ID.</span></span> <span data-ttu-id="2abdd-139">在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2abdd-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="2abdd-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="2abdd-140">*locale*</span></span>     | <span data-ttu-id="2abdd-141">Windows Media Player 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="2abdd-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="2abdd-142">*userlocale*</span><span class="sxs-lookup"><span data-stu-id="2abdd-142">*userlocale*</span></span> | <span data-ttu-id="2abdd-143">Windows 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="2abdd-143">Windows locale ID.</span></span> <span data-ttu-id="2abdd-144">地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。</span><span class="sxs-lookup"><span data-stu-id="2abdd-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="2abdd-145">*version*</span><span class="sxs-lookup"><span data-stu-id="2abdd-145">*version*</span></span>    | <span data-ttu-id="2abdd-146">使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。</span><span class="sxs-lookup"><span data-stu-id="2abdd-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="2abdd-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="2abdd-147">Requirements</span></span>



| <span data-ttu-id="2abdd-148">需求</span><span class="sxs-lookup"><span data-stu-id="2abdd-148">Requirement</span></span> | <span data-ttu-id="2abdd-149">值</span><span class="sxs-lookup"><span data-stu-id="2abdd-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="2abdd-150">版本</span><span class="sxs-lookup"><span data-stu-id="2abdd-150">Version</span></span><br/> | <span data-ttu-id="2abdd-151">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2abdd-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2abdd-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2abdd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abdd-153">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2abdd-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="2abdd-154">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2abdd-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="2abdd-155">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="2abdd-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





