---
title: OnViewChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 當 Windows Media Player 中的 view 變更時，就會發生 OnViewChange 事件。
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- External. OnViewChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986169"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="9e010-106">OnViewChange 事件</span><span class="sxs-lookup"><span data-stu-id="9e010-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="9e010-107">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="9e010-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9e010-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="9e010-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9e010-109">當 Windows Media Player 中的 view 變更時，就會發生 **OnViewChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="9e010-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="9e010-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="9e010-110">Possible Values</span></span>

<span data-ttu-id="9e010-111">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="9e010-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e010-112">參數</span><span class="sxs-lookup"><span data-stu-id="9e010-112">Parameters</span></span>

<span data-ttu-id="9e010-113">處理此事件的函式不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="9e010-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e010-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e010-114">Remarks</span></span>

<span data-ttu-id="9e010-115">Windows Media Player 中的觀點可能會因為下列任何原因而變更：</span><span class="sxs-lookup"><span data-stu-id="9e010-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="9e010-116">使用者會與 Windows Media Player 的使用者介面互動。</span><span class="sxs-lookup"><span data-stu-id="9e010-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="9e010-117">使用者會與探索頁面互動，而 [探索] 頁面上的腳本則會呼叫 [External. changeView](external-changeview.md)。</span><span class="sxs-lookup"><span data-stu-id="9e010-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="9e010-118">使用者會與探索頁面互動，而 [探索] 頁面上的腳本則會呼叫 [External. changeViewOnlineList](external-changeviewonlinelist.md)。</span><span class="sxs-lookup"><span data-stu-id="9e010-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="9e010-119">當 Windows Media Player 中的 view 變更時，播放程式會呼叫 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 來取得下一個探索頁面的 URL，以顯示。</span><span class="sxs-lookup"><span data-stu-id="9e010-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="9e010-120">不過，在播放玩家顯示新的 [探索] 頁面之前，它會引發 **OnViewChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="9e010-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="9e010-121">如果 **OnViewChange** 事件處理常式呼叫 [External. cancelNavigate](external-cancelnavigate.md)，Windows Media Player 不會顯示新的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="9e010-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="9e010-122">相反地，它會繼續顯示目前的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="9e010-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e010-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e010-123">Requirements</span></span>



| <span data-ttu-id="9e010-124">需求</span><span class="sxs-lookup"><span data-stu-id="9e010-124">Requirement</span></span> | <span data-ttu-id="9e010-125">值</span><span class="sxs-lookup"><span data-stu-id="9e010-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e010-126">版本</span><span class="sxs-lookup"><span data-stu-id="9e010-126">Version</span></span><br/> | <span data-ttu-id="9e010-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="9e010-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="9e010-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9e010-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e010-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e010-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e010-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e010-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e010-131">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="9e010-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9e010-132">**ChangeView**</span><span class="sxs-lookup"><span data-stu-id="9e010-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="9e010-133">**ChangeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="9e010-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





