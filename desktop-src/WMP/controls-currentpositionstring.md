---
title: CurrentPositionString
description: CurrentPositionString 屬性會將媒體專案中的目前位置抓取為格式化為 HH MM SS (小時、分鐘和秒) 的字串。
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- CurrentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979540"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="40305-104">CurrentPositionString</span><span class="sxs-lookup"><span data-stu-id="40305-104">Controls.currentPositionString</span></span>

<span data-ttu-id="40305-105">**CurrentPositionString** 屬性會將媒體專案中的目前位置抓取為格式化為 HH： MM： SS (小時、分鐘和秒) 的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="40305-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="40305-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="40305-106">Possible Values</span></span>

<span data-ttu-id="40305-107">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="40305-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40305-108">備註</span><span class="sxs-lookup"><span data-stu-id="40305-108">Remarks</span></span>

<span data-ttu-id="40305-109">如果媒體專案的長度不到一小時，則不會包含 HH：部分。</span><span class="sxs-lookup"><span data-stu-id="40305-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="40305-110">當媒體專案停止或暫停時，您應該包含程式碼以停止計時器。</span><span class="sxs-lookup"><span data-stu-id="40305-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="40305-111">範例</span><span class="sxs-lookup"><span data-stu-id="40305-111">Examples</span></span>

<span data-ttu-id="40305-112">下列 JScript 範例會啟動 HTML 計時器，以一秒的間隔顯示媒體檔案的目前位置。</span><span class="sxs-lookup"><span data-stu-id="40305-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="40305-113">已建立名為 MyText 的 HTML 文字元素，以顯示目前的位置。</span><span class="sxs-lookup"><span data-stu-id="40305-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="40305-114">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="40305-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="40305-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="40305-115">Requirements</span></span>



| <span data-ttu-id="40305-116">需求</span><span class="sxs-lookup"><span data-stu-id="40305-116">Requirement</span></span> | <span data-ttu-id="40305-117">值</span><span class="sxs-lookup"><span data-stu-id="40305-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40305-118">版本</span><span class="sxs-lookup"><span data-stu-id="40305-118">Version</span></span><br/> | <span data-ttu-id="40305-119">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="40305-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="40305-120">DLL</span><span class="sxs-lookup"><span data-stu-id="40305-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="40305-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40305-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40305-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40305-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40305-123">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="40305-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





