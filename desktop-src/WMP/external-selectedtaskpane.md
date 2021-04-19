---
title: SelectedTaskPane
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 SelectedTaskPane 屬性會指定或抓取目前選取的工作窗格。
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- SelectedTaskPane Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998594"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="5637e-106">SelectedTaskPane</span><span class="sxs-lookup"><span data-stu-id="5637e-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="5637e-107">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="5637e-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5637e-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="5637e-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5637e-109">**SelectedTaskPane** 屬性會指定或抓取目前選取的工作窗格。</span><span class="sxs-lookup"><span data-stu-id="5637e-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="5637e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5637e-110">Syntax</span></span>

<span data-ttu-id="5637e-111">SelectedTaskPane = *servicetask*</span><span class="sxs-lookup"><span data-stu-id="5637e-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="5637e-112">可能的值</span><span class="sxs-lookup"><span data-stu-id="5637e-112">Possible Values</span></span>

<span data-ttu-id="5637e-113">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="5637e-113">This property is a read/write **String**.</span></span> <span data-ttu-id="5637e-114">可能的值為 "ServiceTask1"、"ServiceTask2" 和 "ServiceTask3"。</span><span class="sxs-lookup"><span data-stu-id="5637e-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="5637e-115">備註</span><span class="sxs-lookup"><span data-stu-id="5637e-115">Remarks</span></span>

<span data-ttu-id="5637e-116">指定這個屬性的值會反白顯示該窗格的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5637e-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="5637e-117">它不會讓指定的工作窗格變成作用中。</span><span class="sxs-lookup"><span data-stu-id="5637e-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="5637e-118">當頁面載入時，您應該指定此屬性的值，以設定網頁的目前工作窗格按鈕，以確保正確的工作窗格按鈕處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="5637e-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="5637e-119">若要讓特定工作窗格成為使用中的工作窗格，請使用 **NavigateTaskPaneURL** 方法。</span><span class="sxs-lookup"><span data-stu-id="5637e-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5637e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5637e-120">Requirements</span></span>



| <span data-ttu-id="5637e-121">需求</span><span class="sxs-lookup"><span data-stu-id="5637e-121">Requirement</span></span> | <span data-ttu-id="5637e-122">值</span><span class="sxs-lookup"><span data-stu-id="5637e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5637e-123">版本</span><span class="sxs-lookup"><span data-stu-id="5637e-123">Version</span></span><br/> | <span data-ttu-id="5637e-124">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5637e-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="5637e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5637e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5637e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5637e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5637e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5637e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5637e-128">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="5637e-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5637e-129">**NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="5637e-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





