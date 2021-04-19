---
title: 主題. openView
description: OpenView 方法會在新視窗中開啟一個 VIEW。
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- 主題. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001824"
---
# <a name="themeopenview"></a><span data-ttu-id="1c013-104">主題. openView</span><span class="sxs-lookup"><span data-stu-id="1c013-104">THEME.openView</span></span>

<span data-ttu-id="1c013-105">**OpenView** 方法會在新視窗中開啟一個 **VIEW** 。</span><span class="sxs-lookup"><span data-stu-id="1c013-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="1c013-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c013-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c013-107"><span id="view"></span><span id="VIEW"></span>*視圖*</span><span class="sxs-lookup"><span data-stu-id="1c013-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="1c013-108">**字串**，指定要開啟之 **視圖** 的 **識別碼**。</span><span class="sxs-lookup"><span data-stu-id="1c013-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c013-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c013-109">Return Value</span></span>

<span data-ttu-id="1c013-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1c013-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1c013-111">範例</span><span class="sxs-lookup"><span data-stu-id="1c013-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="1c013-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c013-112">Requirements</span></span>



| <span data-ttu-id="1c013-113">需求</span><span class="sxs-lookup"><span data-stu-id="1c013-113">Requirement</span></span> | <span data-ttu-id="1c013-114">值</span><span class="sxs-lookup"><span data-stu-id="1c013-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1c013-115">版本</span><span class="sxs-lookup"><span data-stu-id="1c013-115">Version</span></span><br/> | <span data-ttu-id="1c013-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="1c013-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c013-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c013-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c013-118">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="1c013-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="1c013-119">**CloseView**</span><span class="sxs-lookup"><span data-stu-id="1c013-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="1c013-120">**OpenViewRelative**</span><span class="sxs-lookup"><span data-stu-id="1c013-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





