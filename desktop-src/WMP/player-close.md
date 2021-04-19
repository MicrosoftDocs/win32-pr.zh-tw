---
title: Player. close 方法
description: Close 方法會釋放 Windows Media Player 資源。
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- close 方法 Windows Media Player
- close 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，close 方法
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995793"
---
# <a name="playerclose-method"></a><span data-ttu-id="c3009-106">Player. close 方法</span><span class="sxs-lookup"><span data-stu-id="c3009-106">Player.close method</span></span>

<span data-ttu-id="c3009-107">**Close** 方法會釋放 Windows Media Player 資源。</span><span class="sxs-lookup"><span data-stu-id="c3009-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3009-108">語法</span><span class="sxs-lookup"><span data-stu-id="c3009-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="c3009-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3009-109">Parameters</span></span>

<span data-ttu-id="c3009-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c3009-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3009-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3009-111">Return value</span></span>

<span data-ttu-id="c3009-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3009-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3009-113">備註</span><span class="sxs-lookup"><span data-stu-id="c3009-113">Remarks</span></span>

<span data-ttu-id="c3009-114">這個方法會關閉目前的數位媒體檔案，而不是 Windows Media Player 本身。</span><span class="sxs-lookup"><span data-stu-id="c3009-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="c3009-115">範例</span><span class="sxs-lookup"><span data-stu-id="c3009-115">Examples</span></span>

<span data-ttu-id="c3009-116">下列範例會建立 HTML BUTTON 元素，當按下時，會在 Windows Media Player 中停止播放，並釋放使用中的資源。</span><span class="sxs-lookup"><span data-stu-id="c3009-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="c3009-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c3009-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="c3009-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3009-118">Requirements</span></span>



| <span data-ttu-id="c3009-119">需求</span><span class="sxs-lookup"><span data-stu-id="c3009-119">Requirement</span></span> | <span data-ttu-id="c3009-120">值</span><span class="sxs-lookup"><span data-stu-id="c3009-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3009-121">版本</span><span class="sxs-lookup"><span data-stu-id="c3009-121">Version</span></span><br/> | <span data-ttu-id="c3009-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c3009-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c3009-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3009-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3009-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3009-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3009-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3009-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3009-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="c3009-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





