---
title: TemplateBeingDisplayedInLocalLibrary
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |TemplateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- TemplateBeingDisplayedInLocalLibrary Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978722"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="4da87-105">TemplateBeingDisplayedInLocalLibrary</span><span class="sxs-lookup"><span data-stu-id="4da87-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="4da87-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="4da87-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4da87-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="4da87-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4da87-108">**TemplateBeingDisplayedInLocalLibrary** 屬性會指出目前的 [探索] 頁面所表示的摘要是否正在顯示于 [本機程式庫] 樹狀檢視控制項中。</span><span class="sxs-lookup"><span data-stu-id="4da87-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da87-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4da87-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="4da87-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="4da87-110">Possible Values</span></span>

<span data-ttu-id="4da87-111">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="4da87-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="4da87-112">**TRUE** 表示摘要會顯示在 [本機程式庫] 樹狀檢視控制項中。</span><span class="sxs-lookup"><span data-stu-id="4da87-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da87-113">備註</span><span class="sxs-lookup"><span data-stu-id="4da87-113">Remarks</span></span>

<span data-ttu-id="4da87-114">代表動態播放清單摘要的探索頁面可以顯示一個按鈕，讓使用者在其本機文件庫中「儲存」摘要。</span><span class="sxs-lookup"><span data-stu-id="4da87-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="4da87-115">儲存摘要，在此內容中，表示某些中繼資料會儲存在使用者的電腦上，而且摘要會列在 [本機程式庫] 樹狀檢視中的 [ **播放清單** ] 節點底下。</span><span class="sxs-lookup"><span data-stu-id="4da87-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="4da87-116">[探索] 頁面上的腳本可以檢查 **templateBeingDisplayedInLocalLibrary** 屬性，以判斷使用者是否已將摘要儲存在本機程式庫中。</span><span class="sxs-lookup"><span data-stu-id="4da87-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="4da87-117">如果使用者已經儲存摘要，[探索] 頁面應該不會顯示 [儲存] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4da87-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="4da87-118">代表廣播的探索頁面應該會基於相同的理由檢查 **templateBeingDisplayedInLocalLibrary** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4da87-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da87-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4da87-119">Requirements</span></span>



| <span data-ttu-id="4da87-120">需求</span><span class="sxs-lookup"><span data-stu-id="4da87-120">Requirement</span></span> | <span data-ttu-id="4da87-121">值</span><span class="sxs-lookup"><span data-stu-id="4da87-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4da87-122">版本</span><span class="sxs-lookup"><span data-stu-id="4da87-122">Version</span></span><br/> | <span data-ttu-id="4da87-123">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="4da87-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="4da87-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4da87-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4da87-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4da87-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da87-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4da87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da87-127">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="4da87-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





