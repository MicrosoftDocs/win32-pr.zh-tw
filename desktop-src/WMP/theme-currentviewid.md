---
title: CurrentViewID
description: CurrentViewID 屬性會指定或抓取目前顯示的視圖。
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- CurrentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001828"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="85aa1-104">CurrentViewID</span><span class="sxs-lookup"><span data-stu-id="85aa1-104">THEME.currentViewID</span></span>

<span data-ttu-id="85aa1-105">**CurrentViewID** 屬性會指定或抓取目前顯示的 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="85aa1-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="85aa1-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="85aa1-106">Possible Values</span></span>

<span data-ttu-id="85aa1-107">這個屬性是一個讀取/寫入 **字串**，可指定目前 **視圖** 的 **識別碼**。</span><span class="sxs-lookup"><span data-stu-id="85aa1-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="85aa1-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="85aa1-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85aa1-109">備註</span><span class="sxs-lookup"><span data-stu-id="85aa1-109">Remarks</span></span>

<span data-ttu-id="85aa1-110">指定 **currentViewID** 會自動關閉 **view** global 屬性所指向的現有 **currentView** () 並開啟指定的 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="85aa1-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="85aa1-111">範例</span><span class="sxs-lookup"><span data-stu-id="85aa1-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="85aa1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="85aa1-112">Requirements</span></span>



| <span data-ttu-id="85aa1-113">需求</span><span class="sxs-lookup"><span data-stu-id="85aa1-113">Requirement</span></span> | <span data-ttu-id="85aa1-114">值</span><span class="sxs-lookup"><span data-stu-id="85aa1-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="85aa1-115">版本</span><span class="sxs-lookup"><span data-stu-id="85aa1-115">Version</span></span><br/> | <span data-ttu-id="85aa1-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="85aa1-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85aa1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85aa1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85aa1-118">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="85aa1-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





