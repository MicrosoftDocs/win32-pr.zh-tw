---
title: ChangeView 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ChangeView 方法會在 Windows Media Player 中變更視圖。
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- changeView 方法 Windows Media Player
- changeView 方法 Windows Media Player、External 類別
- External class Windows Media Player，changeView 方法
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986171"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="98866-108">ChangeView 方法</span><span class="sxs-lookup"><span data-stu-id="98866-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="98866-109">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="98866-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="98866-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="98866-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="98866-111">**ChangeView** 方法會在 Windows Media Player 中變更視圖。</span><span class="sxs-lookup"><span data-stu-id="98866-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="98866-112">語法</span><span class="sxs-lookup"><span data-stu-id="98866-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="98866-113">參數</span><span class="sxs-lookup"><span data-stu-id="98866-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98866-114">*LibraryLocationType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98866-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98866-115">指定新檢視類型的連結 [庫位置常數](library-location-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="98866-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="98866-116">例如，常數 CPGenreID 指定新的視圖會顯示特定的內容類型。</span><span class="sxs-lookup"><span data-stu-id="98866-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="98866-117">*LibraryLocationID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98866-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98866-118">**字串** ，包含要在新的視圖中顯示之特定專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98866-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="98866-119">例如，如果 *LibraryLocationType* 是 CPGenreID，則此參數會指定要在新的視圖中顯示之類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="98866-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="98866-120">這個字串可以是空的。</span><span class="sxs-lookup"><span data-stu-id="98866-120">This string can be empty.</span></span> <span data-ttu-id="98866-121">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="98866-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="98866-122">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98866-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98866-123">包含新視圖之篩選準則的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="98866-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="98866-124">此視圖會篩選成使用者已在播放程式的 word 滾輪控制項中輸入此文字。</span><span class="sxs-lookup"><span data-stu-id="98866-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="98866-125">這個字串可以是空的。</span><span class="sxs-lookup"><span data-stu-id="98866-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="98866-126">*ViewParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98866-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98866-127">包含參數的 **字串**，Windows Media Player 可供新的 [探索] 頁面使用，該頁面會以新的視圖顯示。</span><span class="sxs-lookup"><span data-stu-id="98866-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="98866-128">Windows Media Player 不會解讀這些參數。</span><span class="sxs-lookup"><span data-stu-id="98866-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="98866-129">它們是由線上商店所建立，而且只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="98866-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98866-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="98866-130">Return value</span></span>

<span data-ttu-id="98866-131">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="98866-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98866-132">備註</span><span class="sxs-lookup"><span data-stu-id="98866-132">Remarks</span></span>

<span data-ttu-id="98866-133">在某些情況下，將 *LibraryLocationID* 參數設定為空字串是合理的。</span><span class="sxs-lookup"><span data-stu-id="98866-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="98866-134">例如，如果您將 *LibraryLocationType* 參數設定為 AllCPAlbumIDs，則新的視圖會代表所有專輯。</span><span class="sxs-lookup"><span data-stu-id="98866-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="98866-135">沒有任何個別專輯會成為新視圖的焦點，因此不需要在 *LibraryLocationID* 參數中提供專輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="98866-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="98866-136">*ViewParams* 參數提供讓探索頁面與另一個探索頁面通訊的方式。</span><span class="sxs-lookup"><span data-stu-id="98866-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="98866-137">當探索頁面上的腳本呼叫 **changeView** 時，Windows Media Player 會調整其使用者介面。</span><span class="sxs-lookup"><span data-stu-id="98866-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="98866-138">該調整會導致播放程式呼叫外掛程式的 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，以取得新探索頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="98866-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="98866-139">原始探索頁面在 *ViewParams* 參數中傳遞的字串不會傳遞至 **GetTemplate**。</span><span class="sxs-lookup"><span data-stu-id="98866-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="98866-140">不過，新的 [探索] 頁面可以藉由呼叫 [External. viewParameters](external-viewparameters.md)來取出 *ViewParams* 字串。</span><span class="sxs-lookup"><span data-stu-id="98866-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98866-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="98866-141">Requirements</span></span>



| <span data-ttu-id="98866-142">需求</span><span class="sxs-lookup"><span data-stu-id="98866-142">Requirement</span></span> | <span data-ttu-id="98866-143">值</span><span class="sxs-lookup"><span data-stu-id="98866-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98866-144">版本</span><span class="sxs-lookup"><span data-stu-id="98866-144">Version</span></span><br/> | <span data-ttu-id="98866-145">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="98866-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="98866-146">DLL</span><span class="sxs-lookup"><span data-stu-id="98866-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="98866-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98866-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98866-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98866-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98866-149">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="98866-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="98866-150">**ChangeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="98866-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="98866-151">**LibraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="98866-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="98866-152">**LibraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="98866-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="98866-153">**ViewParameters**</span><span class="sxs-lookup"><span data-stu-id="98866-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





