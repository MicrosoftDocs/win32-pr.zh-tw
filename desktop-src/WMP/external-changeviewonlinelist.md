---
title: ChangeViewOnlineList 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ChangeViewOnlineList 方法
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- changeViewOnlineList 方法 Windows Media Player
- changeViewOnlineList 方法 Windows Media Player、External 類別
- External class Windows Media Player，changeViewOnlineList 方法
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980155"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="f0c80-107">ChangeViewOnlineList 方法</span><span class="sxs-lookup"><span data-stu-id="f0c80-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="f0c80-108">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="f0c80-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f0c80-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="f0c80-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f0c80-110">**ChangeViewOnlineList** 方法會在 Windows Media Player 中變更視圖，以顯示線上商店動態產生的清單。</span><span class="sxs-lookup"><span data-stu-id="f0c80-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c80-111">語法</span><span class="sxs-lookup"><span data-stu-id="f0c80-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="f0c80-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0c80-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c80-113">*LibraryLocationType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-114">指定新檢視類型的連結 [庫位置常數](library-location-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="f0c80-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="f0c80-115">例如，常數 CPGenreID 指定新的視圖會顯示特定的內容類型。</span><span class="sxs-lookup"><span data-stu-id="f0c80-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="f0c80-116">*LibraryLocationID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-117">**字串** ，包含要在新的視圖中顯示之特定專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0c80-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="f0c80-118">例如，如果 *LibraryLocationType* 是 CPGenreID，則此參數會指定要在新的視圖中顯示之類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0c80-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="f0c80-119">這個字串可以是空的。</span><span class="sxs-lookup"><span data-stu-id="f0c80-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="f0c80-120">*Params* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-121">包含參數的 **字串**，這些參數會藉由呼叫 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)，Windows Media Player 傳遞到線上商店的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="f0c80-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="f0c80-122">Windows Media Player 不會解讀這些參數。</span><span class="sxs-lookup"><span data-stu-id="f0c80-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="f0c80-123">它們是由線上商店所建立，而且只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="f0c80-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="f0c80-124">這個字串可以是空的</span><span class="sxs-lookup"><span data-stu-id="f0c80-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="f0c80-125">*FriendlyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-126">**字串** ，包含要顯示為動態清單之易記名稱（Windows Media Player）。</span><span class="sxs-lookup"><span data-stu-id="f0c80-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="f0c80-127">*ListType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-128">程式庫位置常數，指定動態產生清單中的專案類型。</span><span class="sxs-lookup"><span data-stu-id="f0c80-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="f0c80-129">例如，如果此參數的值是 CPTrackID，則動態清單將包含追蹤。</span><span class="sxs-lookup"><span data-stu-id="f0c80-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="f0c80-130">*ViewMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c80-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c80-131">**字串** ，指定 Windows Media Player 將用來顯示動態清單的模式。</span><span class="sxs-lookup"><span data-stu-id="f0c80-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="f0c80-132">呼叫端必須將此參數設定為下列其中一個值（定義于 contentpartner 中）：</span><span class="sxs-lookup"><span data-stu-id="f0c80-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="f0c80-133">ViewModeReport</span><span class="sxs-lookup"><span data-stu-id="f0c80-133">ViewModeReport</span></span>

<span data-ttu-id="f0c80-134">ViewModeDetails</span><span class="sxs-lookup"><span data-stu-id="f0c80-134">ViewModeDetails</span></span>

<span data-ttu-id="f0c80-135">ViewModeIcon</span><span class="sxs-lookup"><span data-stu-id="f0c80-135">ViewModeIcon</span></span>

<span data-ttu-id="f0c80-136">ViewModeTile</span><span class="sxs-lookup"><span data-stu-id="f0c80-136">ViewModeTile</span></span>

<span data-ttu-id="f0c80-137">ViewModeOrderedList</span><span class="sxs-lookup"><span data-stu-id="f0c80-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c80-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0c80-138">Return value</span></span>

<span data-ttu-id="f0c80-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f0c80-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c80-140">備註</span><span class="sxs-lookup"><span data-stu-id="f0c80-140">Remarks</span></span>

<span data-ttu-id="f0c80-141">當探索頁面上的腳本呼叫 **changeViewOnlineList** 時，Windows Media Player 會將部分參數傳遞至 [IWMPContentPartner：： GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) 和 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，這些方法是由線上商店的外掛程式所執行。</span><span class="sxs-lookup"><span data-stu-id="f0c80-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="f0c80-142">下表顯示這三種方法的參數之間的對應。</span><span class="sxs-lookup"><span data-stu-id="f0c80-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="f0c80-143">changeViewOnlineList 參數</span><span class="sxs-lookup"><span data-stu-id="f0c80-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="f0c80-144">GetListContents 參數</span><span class="sxs-lookup"><span data-stu-id="f0c80-144">GetListContents parameter</span></span> | <span data-ttu-id="f0c80-145">GetTemplate 參數</span><span class="sxs-lookup"><span data-stu-id="f0c80-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="f0c80-146">*LocationType*</span><span class="sxs-lookup"><span data-stu-id="f0c80-146">*LocationType*</span></span>                 | <span data-ttu-id="f0c80-147">*location*</span><span class="sxs-lookup"><span data-stu-id="f0c80-147">*location*</span></span>                | <span data-ttu-id="f0c80-148">*location*</span><span class="sxs-lookup"><span data-stu-id="f0c80-148">*location*</span></span>            |
| <span data-ttu-id="f0c80-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="f0c80-149">*LocationID*</span></span>                   | <span data-ttu-id="f0c80-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="f0c80-150">*pContext*</span></span>                | <span data-ttu-id="f0c80-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="f0c80-151">*pContext*</span></span>            |
| <span data-ttu-id="f0c80-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="f0c80-152">*Params*</span></span>                       | <span data-ttu-id="f0c80-153">*bstrParams*</span><span class="sxs-lookup"><span data-stu-id="f0c80-153">*bstrParams*</span></span>              | <span data-ttu-id="f0c80-154">*bstrViewParams*</span><span class="sxs-lookup"><span data-stu-id="f0c80-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="f0c80-155">*ListType*</span><span class="sxs-lookup"><span data-stu-id="f0c80-155">*ListType*</span></span>                     | <span data-ttu-id="f0c80-156">*bstrListType*</span><span class="sxs-lookup"><span data-stu-id="f0c80-156">*bstrListType*</span></span>            | <span data-ttu-id="f0c80-157">不適用</span><span class="sxs-lookup"><span data-stu-id="f0c80-157">not applicable</span></span>        |



 

<span data-ttu-id="f0c80-158">由於上表所示的三個方法都是由線上商店所執行，因此您在使用參數時有一些彈性。</span><span class="sxs-lookup"><span data-stu-id="f0c80-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="f0c80-159">其概念是，您會提供足夠的資訊供 **GetListContents** 用來判斷應取得的清單，以及讓 **GetTemplate** 判斷接下來應顯示的探索頁面。</span><span class="sxs-lookup"><span data-stu-id="f0c80-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="f0c80-160">下列範例說明兩個可能性。</span><span class="sxs-lookup"><span data-stu-id="f0c80-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="f0c80-161">**範例1：在線上商店的目錄中的動態清單**</span><span class="sxs-lookup"><span data-stu-id="f0c80-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="f0c80-162">假設您想要讓外掛程式取得線上商店目錄中識別碼為6的動態清單內容。</span><span class="sxs-lookup"><span data-stu-id="f0c80-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="f0c80-163">假設 list 6 是一份曲目清單。</span><span class="sxs-lookup"><span data-stu-id="f0c80-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="f0c80-164">您可以進行下列呼叫，以提供外掛程式足夠的資訊。</span><span class="sxs-lookup"><span data-stu-id="f0c80-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="f0c80-165">請注意， *Params* 參數是空的;外掛程式在其他參數中有足夠的資訊。</span><span class="sxs-lookup"><span data-stu-id="f0c80-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="f0c80-166">**範例2：不在線上商店目錄中的動態清單**</span><span class="sxs-lookup"><span data-stu-id="f0c80-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="f0c80-167">假設您想要讓外掛程式取得不在線上商店目錄中之動態清單的內容。</span><span class="sxs-lookup"><span data-stu-id="f0c80-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="f0c80-168">或許您已決定有動態清單，其中包含特定演出者挑選的歌曲。</span><span class="sxs-lookup"><span data-stu-id="f0c80-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="f0c80-169">假設演出者在線上商店的目錄中有2個識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0c80-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="f0c80-170">您可以進行下列呼叫。</span><span class="sxs-lookup"><span data-stu-id="f0c80-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="f0c80-171">請注意， *LocationType* 和 *LocationID* 參數不會指定清單。</span><span class="sxs-lookup"><span data-stu-id="f0c80-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="f0c80-172">相反地， *Params* 參數會指定清單。</span><span class="sxs-lookup"><span data-stu-id="f0c80-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="f0c80-173">*LocationType* 和 *LocationID* 參數會傳遞至 **IWMPContentPartner：： GetListContents**，但是在此情況下， **GetListContents** 可以忽略它們。</span><span class="sxs-lookup"><span data-stu-id="f0c80-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="f0c80-174">*LocationType* 和 *LocationID* 參數也會傳遞至 **IWMPContentPartner：： GetTemplate**，這可以用來判斷應該使用動態清單來顯示的 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f0c80-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c80-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0c80-175">Requirements</span></span>



| <span data-ttu-id="f0c80-176">需求</span><span class="sxs-lookup"><span data-stu-id="f0c80-176">Requirement</span></span> | <span data-ttu-id="f0c80-177">值</span><span class="sxs-lookup"><span data-stu-id="f0c80-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c80-178">版本</span><span class="sxs-lookup"><span data-stu-id="f0c80-178">Version</span></span><br/> | <span data-ttu-id="f0c80-179">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="f0c80-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="f0c80-180">DLL</span><span class="sxs-lookup"><span data-stu-id="f0c80-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0c80-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c80-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c80-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0c80-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c80-183">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="f0c80-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f0c80-184">**IWMPContentPartner::GetListContents**</span><span class="sxs-lookup"><span data-stu-id="f0c80-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="f0c80-185">**IWMPContentPartnerCallback::AddListContents**</span><span class="sxs-lookup"><span data-stu-id="f0c80-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="f0c80-186">**IWMPContentPartner::GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="f0c80-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="f0c80-187">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="f0c80-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





