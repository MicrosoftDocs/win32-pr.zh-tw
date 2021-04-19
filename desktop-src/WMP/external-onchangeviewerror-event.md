---
title: OnChangeViewError 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnChangeViewError 事件
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- External. OnChangeViewError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001140"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="9061e-105">OnChangeViewError 事件</span><span class="sxs-lookup"><span data-stu-id="9061e-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="9061e-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="9061e-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9061e-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="9061e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9061e-108">當 [changeView](external-changeview.md)方法的呼叫產生錯誤時，就會發生 **OnChangeViewError** 事件。</span><span class="sxs-lookup"><span data-stu-id="9061e-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="9061e-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="9061e-109">Possible Values</span></span>

<span data-ttu-id="9061e-110">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="9061e-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="9061e-111">參數</span><span class="sxs-lookup"><span data-stu-id="9061e-111">Parameters</span></span>

<span data-ttu-id="9061e-112">處理此事件的函式具有下列參數。</span><span class="sxs-lookup"><span data-stu-id="9061e-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="9061e-113"><span id="hr"></span><span id="HR"></span>*人力資源*</span><span class="sxs-lookup"><span data-stu-id="9061e-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="9061e-114">**HRESULT** 失敗代碼，指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="9061e-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="9061e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="9061e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="9061e-116">在 **changeView** 的 **LibraryLocationType** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="9061e-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="9061e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="9061e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="9061e-118">在 **changeView** 的 **LibraryLocationID** 參數中傳遞的相同字串 thatwas。</span><span class="sxs-lookup"><span data-stu-id="9061e-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="9061e-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*濾波器*</span><span class="sxs-lookup"><span data-stu-id="9061e-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="9061e-120">在 **changeView** 的 **篩選** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="9061e-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="9061e-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span><span class="sxs-lookup"><span data-stu-id="9061e-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="9061e-122">在 **changeView** 的 **ViewParams** 參數中傳遞的相同字串。</span><span class="sxs-lookup"><span data-stu-id="9061e-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9061e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9061e-123">Requirements</span></span>



| <span data-ttu-id="9061e-124">需求</span><span class="sxs-lookup"><span data-stu-id="9061e-124">Requirement</span></span> | <span data-ttu-id="9061e-125">值</span><span class="sxs-lookup"><span data-stu-id="9061e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9061e-126">版本</span><span class="sxs-lookup"><span data-stu-id="9061e-126">Version</span></span><br/> | <span data-ttu-id="9061e-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="9061e-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="9061e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9061e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9061e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9061e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9061e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9061e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9061e-131">**類型1線上商店的 ExternalObject**</span><span class="sxs-lookup"><span data-stu-id="9061e-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





