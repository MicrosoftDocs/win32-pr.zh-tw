---
title: OnChangeViewOnlineListError 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnChangeViewOnlineListError 事件
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- External. OnChangeViewOnlineListError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983150"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="1609a-105">OnChangeViewOnlineListError 事件</span><span class="sxs-lookup"><span data-stu-id="1609a-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="1609a-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="1609a-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1609a-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="1609a-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1609a-108">當 [changeViewOnlineList](external-changeviewonlinelist.md)方法的呼叫產生錯誤時，就會發生 **OnChangeViewOnlineListError** 事件。</span><span class="sxs-lookup"><span data-stu-id="1609a-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="1609a-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="1609a-109">Possible Values</span></span>

<span data-ttu-id="1609a-110">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="1609a-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="1609a-111">參數</span><span class="sxs-lookup"><span data-stu-id="1609a-111">Parameters</span></span>

<span data-ttu-id="1609a-112">處理此錯誤的函式具有下列參數。</span><span class="sxs-lookup"><span data-stu-id="1609a-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="1609a-113"><span id="hr"></span><span id="HR"></span>*人力資源*</span><span class="sxs-lookup"><span data-stu-id="1609a-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-114">**HRESULT** 失敗代碼，指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="1609a-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="1609a-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-116">在 **changeViewOnlineList** 的 **LibraryLocationType** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="1609a-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-118">在 **changeViewOnlineList** 的 **LibraryLocationID** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="1609a-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-120">在 **changeViewOnlineList** 的 **Params** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*友好*</span><span class="sxs-lookup"><span data-stu-id="1609a-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-122">在 **changeViewOnlineList** 的 **FriendlyName** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span><span class="sxs-lookup"><span data-stu-id="1609a-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-124">在 **changeViewOnlineList** 的 **ListType** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="1609a-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="1609a-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="1609a-126">在 **changeViewOnlineList** 的 **ViewMode** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="1609a-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1609a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1609a-127">Requirements</span></span>



| <span data-ttu-id="1609a-128">需求</span><span class="sxs-lookup"><span data-stu-id="1609a-128">Requirement</span></span> | <span data-ttu-id="1609a-129">值</span><span class="sxs-lookup"><span data-stu-id="1609a-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1609a-130">版本</span><span class="sxs-lookup"><span data-stu-id="1609a-130">Version</span></span><br/> | <span data-ttu-id="1609a-131">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1609a-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="1609a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1609a-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="1609a-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1609a-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1609a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1609a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1609a-135">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="1609a-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





