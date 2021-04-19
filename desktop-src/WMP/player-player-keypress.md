---
title: Player. KeyPress 事件
description: 按下並釋放按鍵時，就會發生 KeyPress 事件。 |Player. KeyPress 事件
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- 按鍵事件 Windows Media Player
- KeyPress 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player，按鍵事件
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994634"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="d3cf4-107">Player. KeyPress 事件</span><span class="sxs-lookup"><span data-stu-id="d3cf4-107">Player.KeyPress event</span></span>

<span data-ttu-id="d3cf4-108">按下並釋放按鍵時，就會發生 **KeyPress** 事件。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cf4-109">語法</span><span class="sxs-lookup"><span data-stu-id="d3cf4-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="d3cf4-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3cf4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3cf4-111">*nKeyAscii*</span><span class="sxs-lookup"><span data-stu-id="d3cf4-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="d3cf4-112">**數位** (**int**) 指定字元的標準數值 ANSI 代碼。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3cf4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3cf4-113">Return value</span></span>

<span data-ttu-id="d3cf4-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3cf4-115">備註</span><span class="sxs-lookup"><span data-stu-id="d3cf4-115">Remarks</span></span>

<span data-ttu-id="d3cf4-116">當擊鍵產生任何可列印的鍵盤字元、CTRL 鍵與標準字母中的字元或一些特殊字元的其中一個字元，以及 ENTER 鍵或倒退鍵時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="d3cf4-117">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d3cf4-118">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d3cf4-119">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cf4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3cf4-120">Requirements</span></span>



| <span data-ttu-id="d3cf4-121">需求</span><span class="sxs-lookup"><span data-stu-id="d3cf4-121">Requirement</span></span> | <span data-ttu-id="d3cf4-122">值</span><span class="sxs-lookup"><span data-stu-id="d3cf4-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cf4-123">版本</span><span class="sxs-lookup"><span data-stu-id="d3cf4-123">Version</span></span><br/> | <span data-ttu-id="d3cf4-124">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="d3cf4-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d3cf4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3cf4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3cf4-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3cf4-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3cf4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3cf4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3cf4-128">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="d3cf4-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





