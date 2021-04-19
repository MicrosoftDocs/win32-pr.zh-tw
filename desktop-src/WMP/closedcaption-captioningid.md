---
title: ClosedCaption.captioningID
description: CaptioningID 屬性會指定或抓取顯示字幕的元素名稱。
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption. captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981087"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="152a6-104">ClosedCaption.captioningID</span><span class="sxs-lookup"><span data-stu-id="152a6-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="152a6-105">**CaptioningID** 屬性會指定或抓取顯示字幕的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="152a6-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="152a6-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="152a6-106">Possible Values</span></span>

<span data-ttu-id="152a6-107">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="152a6-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="152a6-108">備註</span><span class="sxs-lookup"><span data-stu-id="152a6-108">Remarks</span></span>

<span data-ttu-id="152a6-109">指定的元素名稱可以是網頁中的任何 HTML 專案，只要它支援 innerHTML 屬性即可。</span><span class="sxs-lookup"><span data-stu-id="152a6-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="152a6-110">如果網頁包含多個框架，元素名稱只能參考與播放機控制項相同框架中的元素。</span><span class="sxs-lookup"><span data-stu-id="152a6-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="152a6-111">**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="152a6-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="152a6-112">範例</span><span class="sxs-lookup"><span data-stu-id="152a6-112">Examples</span></span>

<span data-ttu-id="152a6-113">下列 Microsoft JScript 範例使用 *ClosedCaption*。**captioningID** ，選擇用來顯示標題的網頁區域。</span><span class="sxs-lookup"><span data-stu-id="152a6-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="152a6-114">已建立兩個 HTML DIV 元素，分別具有 ID = CC1 和 ID = CC2。</span><span class="sxs-lookup"><span data-stu-id="152a6-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="152a6-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="152a6-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="152a6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="152a6-116">Requirements</span></span>



| <span data-ttu-id="152a6-117">需求</span><span class="sxs-lookup"><span data-stu-id="152a6-117">Requirement</span></span> | <span data-ttu-id="152a6-118">值</span><span class="sxs-lookup"><span data-stu-id="152a6-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="152a6-119">版本</span><span class="sxs-lookup"><span data-stu-id="152a6-119">Version</span></span><br/> | <span data-ttu-id="152a6-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="152a6-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="152a6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="152a6-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="152a6-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="152a6-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152a6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="152a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152a6-124">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="152a6-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="152a6-125">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="152a6-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





