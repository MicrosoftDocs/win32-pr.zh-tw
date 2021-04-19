---
title: CancelNavigate 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |CancelNavigate 方法
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- cancelNavigate 方法 Windows Media Player
- cancelNavigate 方法 Windows Media Player、External 類別
- External class Windows Media Player，cancelNavigate 方法
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000465"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="d3aed-107">CancelNavigate 方法</span><span class="sxs-lookup"><span data-stu-id="d3aed-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="d3aed-108">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="d3aed-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d3aed-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="d3aed-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d3aed-110">**CancelNavigate** 方法會通知 Windows Media Player，即使播放程式中的視圖已經變更，也不應該顯示新的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3aed-111">語法</span><span class="sxs-lookup"><span data-stu-id="d3aed-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="d3aed-112">參數</span><span class="sxs-lookup"><span data-stu-id="d3aed-112">Parameters</span></span>

<span data-ttu-id="d3aed-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d3aed-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3aed-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3aed-114">Return value</span></span>

<span data-ttu-id="d3aed-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3aed-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3aed-116">備註</span><span class="sxs-lookup"><span data-stu-id="d3aed-116">Remarks</span></span>

<span data-ttu-id="d3aed-117">當 Windows Media Player 的視圖變更時，播放程式會呼叫線上商店的外掛程式，以決定接下來要顯示的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="d3aed-118">不過，在某些情況下，線上商店可能會想要讓播放機繼續顯示現有的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="d3aed-119">下列程式會決定播放程式是否顯示新的探索頁面：</span><span class="sxs-lookup"><span data-stu-id="d3aed-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="d3aed-120">使用者在播放程式的使用者介面或 [探索] 頁面上執行的動作，會要求播放程式變更其觀點。</span><span class="sxs-lookup"><span data-stu-id="d3aed-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="d3aed-121">播放程式會呼叫外掛程式的 [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，以決定接下來要顯示的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="d3aed-122">播放程式會儲存新探索頁面的 URL，但目前不會顯示新的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="d3aed-123">Player 會引發 [OnViewChange](external-onviewchange-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d3aed-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="d3aed-124">如果 [探索] 頁面上的 **OnViewChange** 事件處理常式呼叫 **cancelNavigate**，播放程式就不會顯示新的 [探索] 頁面 (在步驟 2) 中決定。</span><span class="sxs-lookup"><span data-stu-id="d3aed-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="d3aed-125">相反地，它會繼續顯示現有的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="d3aed-126">如果 **OnViewChange** 事件處理常式未呼叫 **cancelNavigate**，播放程式會顯示新的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="d3aed-127">例如，假設播放程式目前顯示已選取特定播放軌的專輯視圖。</span><span class="sxs-lookup"><span data-stu-id="d3aed-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="d3aed-128">也假設目前的 [探索] 頁面是代表整個專輯的頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="d3aed-129">如果使用者按一下同一個專輯的不同曲目，播放程式的視圖會稍微變更，以顯示已選取新的曲目。</span><span class="sxs-lookup"><span data-stu-id="d3aed-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="d3aed-130">但不需要顯示新的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="d3aed-131">代表整個專輯的 [探索] 頁面仍是播放程式顯示的適當頁面。</span><span class="sxs-lookup"><span data-stu-id="d3aed-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3aed-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3aed-132">Requirements</span></span>



| <span data-ttu-id="d3aed-133">需求</span><span class="sxs-lookup"><span data-stu-id="d3aed-133">Requirement</span></span> | <span data-ttu-id="d3aed-134">值</span><span class="sxs-lookup"><span data-stu-id="d3aed-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3aed-135">版本</span><span class="sxs-lookup"><span data-stu-id="d3aed-135">Version</span></span><br/> | <span data-ttu-id="d3aed-136">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="d3aed-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="d3aed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d3aed-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3aed-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3aed-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3aed-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3aed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3aed-140">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="d3aed-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d3aed-141">**ChangeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="d3aed-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="d3aed-142">**OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="d3aed-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





