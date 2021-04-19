---
title: AxWindowsMediaPlayer 物件的按鍵事件
description: 按下並釋放按鍵時，就會發生 KeyPress 事件。 |AxWindowsMediaPlayer 物件的按鍵事件
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- AxWindowsMediaPlayer 物件的按鍵事件 Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995043"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f47d8-105">AxWindowsMediaPlayer 物件的按鍵事件</span><span class="sxs-lookup"><span data-stu-id="f47d8-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f47d8-106">按下並釋放按鍵時，就會發生 KeyPress 事件。</span><span class="sxs-lookup"><span data-stu-id="f47d8-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="f47d8-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="f47d8-107">Event Data</span></span>

<span data-ttu-id="f47d8-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ KeyPressEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="f47d8-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="f47d8-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ KeyPressEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f47d8-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f47d8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f47d8-110">Property</span></span>      | <span data-ttu-id="f47d8-111">描述</span><span class="sxs-lookup"><span data-stu-id="f47d8-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f47d8-112">**nKeyAscii**</span><span class="sxs-lookup"><span data-stu-id="f47d8-112">**nKeyAscii**</span></span> | <span data-ttu-id="f47d8-113">Int16Specifies 字元的標準數值 ANSI 代碼。</span><span class="sxs-lookup"><span data-stu-id="f47d8-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f47d8-114">備註</span><span class="sxs-lookup"><span data-stu-id="f47d8-114">Remarks</span></span>

<span data-ttu-id="f47d8-115">當擊鍵產生任何可列印的鍵盤字元、CTRL 鍵與標準字母中的字元或一些特殊字元的其中一個字元，以及 ENTER 鍵或倒退鍵時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="f47d8-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47d8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f47d8-116">Requirements</span></span>



| <span data-ttu-id="f47d8-117">需求</span><span class="sxs-lookup"><span data-stu-id="f47d8-117">Requirement</span></span> | <span data-ttu-id="f47d8-118">值</span><span class="sxs-lookup"><span data-stu-id="f47d8-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f47d8-119">版本</span><span class="sxs-lookup"><span data-stu-id="f47d8-119">Version</span></span><br/>   | <span data-ttu-id="f47d8-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f47d8-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f47d8-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="f47d8-121">Namespace</span></span><br/> | <span data-ttu-id="f47d8-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f47d8-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f47d8-123">組件</span><span class="sxs-lookup"><span data-stu-id="f47d8-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f47d8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f47d8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47d8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f47d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47d8-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f47d8-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





