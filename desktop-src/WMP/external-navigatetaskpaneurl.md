---
title: NavigateTaskPaneURL 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |NavigateTaskPaneURL 方法
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- NavigateTaskPaneURL 方法 Windows Media Player
- NavigateTaskPaneURL 方法 Windows Media Player、External 類別
- External class Windows Media Player，NavigateTaskPaneURL 方法
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986586"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="a4d84-107">NavigateTaskPaneURL 方法</span><span class="sxs-lookup"><span data-stu-id="a4d84-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="a4d84-108">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="a4d84-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a4d84-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="a4d84-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a4d84-110">**NavigateTaskPaneURL** 方法會在指定的工作窗格中開啟網頁，並將焦點變更至指定的窗格。</span><span class="sxs-lookup"><span data-stu-id="a4d84-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d84-111">語法</span><span class="sxs-lookup"><span data-stu-id="a4d84-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="a4d84-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4d84-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d84-113">*bstrKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d84-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d84-114">**字串** ，包含線上商店的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d84-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="a4d84-115">(必要)</span><span class="sxs-lookup"><span data-stu-id="a4d84-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="a4d84-116">*bstrTaskPane* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d84-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d84-117">包含網頁開啟之工作窗格名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a4d84-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="a4d84-118">(必要)</span><span class="sxs-lookup"><span data-stu-id="a4d84-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="a4d84-119">*bstrParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d84-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d84-120">**字串** ，其中包含要附加至 ServiceInfo 檔的 **導覽** 元素所指定之 URL 的查詢字串參數。</span><span class="sxs-lookup"><span data-stu-id="a4d84-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="a4d84-121">(選用)</span><span class="sxs-lookup"><span data-stu-id="a4d84-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d84-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4d84-122">Return value</span></span>

<span data-ttu-id="a4d84-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4d84-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d84-124">備註</span><span class="sxs-lookup"><span data-stu-id="a4d84-124">Remarks</span></span>

<span data-ttu-id="a4d84-125">流覽至您的線上商店不支援的窗格，可能會導致目前的線上商店變更。</span><span class="sxs-lookup"><span data-stu-id="a4d84-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="a4d84-126">只有當從線上商店提供的網頁呼叫 **NavigateTaskPaneURL** 時，才會對 *bstrParams* 指定的值有效。</span><span class="sxs-lookup"><span data-stu-id="a4d84-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="a4d84-127">下表列出 *bstrTaskPane* 的有效值和各自的相關工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a4d84-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="a4d84-128">值</span><span class="sxs-lookup"><span data-stu-id="a4d84-128">Value</span></span>            | <span data-ttu-id="a4d84-129">工作窗格</span><span class="sxs-lookup"><span data-stu-id="a4d84-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="a4d84-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="a4d84-130">**ServiceTask1**</span></span> | <span data-ttu-id="a4d84-131">第一個線上商店工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a4d84-131">First online store task pane.</span></span>  |
| <span data-ttu-id="a4d84-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="a4d84-132">**ServiceTask2**</span></span> | <span data-ttu-id="a4d84-133">第二個線上商店工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a4d84-133">Second online store task pane.</span></span> |
| <span data-ttu-id="a4d84-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="a4d84-134">**ServiceTask3**</span></span> | <span data-ttu-id="a4d84-135">第三個線上商店工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a4d84-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="a4d84-136">載入時，您的網頁程式碼應該指定 [SelectedTaskPane](external-selectedtaskpane.md) 的值，以確保在導覽完成之後，會反白顯示正確的工作窗格按鈕。</span><span class="sxs-lookup"><span data-stu-id="a4d84-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="a4d84-137">範例</span><span class="sxs-lookup"><span data-stu-id="a4d84-137">Examples</span></span>

<span data-ttu-id="a4d84-138">下列範例程式碼示範 **NavigateTaskPaneURL** 如何建立要針對 **ServiceTask1** 顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="a4d84-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="a4d84-139">**導覽** 元素的範例：</span><span class="sxs-lookup"><span data-stu-id="a4d84-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="a4d84-140">呼叫 **NavigateTaskPaneURL** 方法的範例：</span><span class="sxs-lookup"><span data-stu-id="a4d84-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="a4d84-141">**ServiceTask1** 中顯示的網頁所產生的 URL 範例：</span><span class="sxs-lookup"><span data-stu-id="a4d84-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="a4d84-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4d84-142">Requirements</span></span>



| <span data-ttu-id="a4d84-143">需求</span><span class="sxs-lookup"><span data-stu-id="a4d84-143">Requirement</span></span> | <span data-ttu-id="a4d84-144">值</span><span class="sxs-lookup"><span data-stu-id="a4d84-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d84-145">版本</span><span class="sxs-lookup"><span data-stu-id="a4d84-145">Version</span></span><br/> | <span data-ttu-id="a4d84-146">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4d84-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="a4d84-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d84-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4d84-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d84-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d84-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4d84-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d84-150">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="a4d84-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a4d84-151">**SelectedTaskPane**</span><span class="sxs-lookup"><span data-stu-id="a4d84-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





