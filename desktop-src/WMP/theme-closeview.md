---
title: CloseView
description: CloseView 方法會關閉開啟的視圖。
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- CloseView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998785"
---
# <a name="themecloseview"></a><span data-ttu-id="cfcb1-104">CloseView</span><span class="sxs-lookup"><span data-stu-id="cfcb1-104">THEME.closeView</span></span>

<span data-ttu-id="cfcb1-105">**CloseView** 方法會關閉開啟的 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="cfcb1-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="cfcb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfcb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfcb1-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span><span class="sxs-lookup"><span data-stu-id="cfcb1-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="cfcb1-108">**字串**，指定要關閉之 **視圖** 的 **識別碼**。</span><span class="sxs-lookup"><span data-stu-id="cfcb1-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfcb1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfcb1-109">Return Value</span></span>

<span data-ttu-id="cfcb1-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cfcb1-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="cfcb1-111">範例</span><span class="sxs-lookup"><span data-stu-id="cfcb1-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="cfcb1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfcb1-112">Requirements</span></span>



| <span data-ttu-id="cfcb1-113">需求</span><span class="sxs-lookup"><span data-stu-id="cfcb1-113">Requirement</span></span> | <span data-ttu-id="cfcb1-114">值</span><span class="sxs-lookup"><span data-stu-id="cfcb1-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cfcb1-115">版本</span><span class="sxs-lookup"><span data-stu-id="cfcb1-115">Version</span></span><br/> | <span data-ttu-id="cfcb1-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="cfcb1-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfcb1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfcb1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcb1-118">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="cfcb1-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="cfcb1-119">**主題. openView**</span><span class="sxs-lookup"><span data-stu-id="cfcb1-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





