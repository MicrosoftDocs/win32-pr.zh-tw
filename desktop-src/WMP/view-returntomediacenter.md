---
title: ReturnToMediaCenter
description: ReturnToMediaCenter 方法會將使用者返回 Windows Media Player 的完整模式。
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- ReturnToMediaCenter Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977756"
---
# <a name="viewreturntomediacenter"></a><span data-ttu-id="19fc0-104">ReturnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="19fc0-104">VIEW.returnToMediaCenter</span></span>

<span data-ttu-id="19fc0-105">**ReturnToMediaCenter** 方法會將使用者返回 Windows Media Player 的完整模式。</span><span class="sxs-lookup"><span data-stu-id="19fc0-105">The **returnToMediaCenter** method returns the user to the full mode of Windows Media Player.</span></span>

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a><span data-ttu-id="19fc0-106">參數</span><span class="sxs-lookup"><span data-stu-id="19fc0-106">Parameters</span></span>

<span data-ttu-id="19fc0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="19fc0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19fc0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="19fc0-108">Return Value</span></span>

<span data-ttu-id="19fc0-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19fc0-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="19fc0-110">範例</span><span class="sxs-lookup"><span data-stu-id="19fc0-110">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="19fc0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="19fc0-111">Requirements</span></span>



| <span data-ttu-id="19fc0-112">需求</span><span class="sxs-lookup"><span data-stu-id="19fc0-112">Requirement</span></span> | <span data-ttu-id="19fc0-113">值</span><span class="sxs-lookup"><span data-stu-id="19fc0-113">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="19fc0-114">版本</span><span class="sxs-lookup"><span data-stu-id="19fc0-114">Version</span></span><br/> | <span data-ttu-id="19fc0-115">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="19fc0-115">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19fc0-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19fc0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fc0-117">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="19fc0-117">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





