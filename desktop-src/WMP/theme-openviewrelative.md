---
title: OpenViewRelative
description: OpenViewRelative 方法會在相對於面板左上角的指定初始位置，在新視窗中開啟一個 VIEW。
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- OpenViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999236"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="78c26-104">OpenViewRelative</span><span class="sxs-lookup"><span data-stu-id="78c26-104">THEME.openViewRelative</span></span>

<span data-ttu-id="78c26-105">**OpenViewRelative** 方法會在相對於面板左上角的指定初始位置，在新視窗中開啟一個 **VIEW** 。</span><span class="sxs-lookup"><span data-stu-id="78c26-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="78c26-106">參數</span><span class="sxs-lookup"><span data-stu-id="78c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c26-107"><span id="view"></span><span id="VIEW"></span>*視圖*</span><span class="sxs-lookup"><span data-stu-id="78c26-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="78c26-108">**字串**，指定要開啟之 **視圖** 的 **識別碼**。</span><span class="sxs-lookup"><span data-stu-id="78c26-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="78c26-109"><span id="left"></span><span id="LEFT"></span>*離開*</span><span class="sxs-lookup"><span data-stu-id="78c26-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="78c26-110">**數位** (**long**) 指定外觀左邊框線的初始距離（以圖元為單位）  。</span><span class="sxs-lookup"><span data-stu-id="78c26-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="78c26-111">負數值表示外觀框線左邊的初始位置。</span><span class="sxs-lookup"><span data-stu-id="78c26-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="78c26-112"><span id="top"></span><span id="TOP"></span>*返回頁首*</span><span class="sxs-lookup"><span data-stu-id="78c26-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="78c26-113">**數位** (**Long**) 指定 **視圖** 的上框線相對於面板上框線的初始位置。</span><span class="sxs-lookup"><span data-stu-id="78c26-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="78c26-114">負數值表示外觀框線上方的初始位置。</span><span class="sxs-lookup"><span data-stu-id="78c26-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c26-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="78c26-115">Return Value</span></span>

<span data-ttu-id="78c26-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="78c26-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78c26-117">備註</span><span class="sxs-lookup"><span data-stu-id="78c26-117">Remarks</span></span>

<span data-ttu-id="78c26-118">第一次呼叫這個方法時，會使用針對 **view** 指定的位置，之後使用者可以將 **視圖** 拖曳至另一個位置。</span><span class="sxs-lookup"><span data-stu-id="78c26-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="78c26-119">儲存新的位置，並在後續的呼叫中使用最新的位置。</span><span class="sxs-lookup"><span data-stu-id="78c26-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="78c26-120">範例</span><span class="sxs-lookup"><span data-stu-id="78c26-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="78c26-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="78c26-121">Requirements</span></span>



| <span data-ttu-id="78c26-122">需求</span><span class="sxs-lookup"><span data-stu-id="78c26-122">Requirement</span></span> | <span data-ttu-id="78c26-123">值</span><span class="sxs-lookup"><span data-stu-id="78c26-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="78c26-124">版本</span><span class="sxs-lookup"><span data-stu-id="78c26-124">Version</span></span><br/> | <span data-ttu-id="78c26-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="78c26-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78c26-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78c26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c26-127">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="78c26-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="78c26-128">**CloseView**</span><span class="sxs-lookup"><span data-stu-id="78c26-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="78c26-129">**主題. openView**</span><span class="sxs-lookup"><span data-stu-id="78c26-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





