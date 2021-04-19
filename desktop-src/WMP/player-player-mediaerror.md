---
title: MediaError 事件
description: 當媒體物件有錯誤情況時，就會發生 MediaError 事件。
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- MediaError 事件 Windows Media Player
- MediaError 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaError 事件
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978402"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="0d11f-106">MediaError 事件</span><span class="sxs-lookup"><span data-stu-id="0d11f-106">Player.MediaError event</span></span>

<span data-ttu-id="0d11f-107">當 **媒體** 物件有錯誤情況時，就會發生 **MediaError** 事件。</span><span class="sxs-lookup"><span data-stu-id="0d11f-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d11f-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d11f-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="0d11f-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d11f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d11f-110">*pMediaObject*</span><span class="sxs-lookup"><span data-stu-id="0d11f-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="0d11f-111">具有錯誤狀況的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="0d11f-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d11f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d11f-112">Return value</span></span>

<span data-ttu-id="0d11f-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d11f-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d11f-114">備註</span><span class="sxs-lookup"><span data-stu-id="0d11f-114">Remarks</span></span>

<span data-ttu-id="0d11f-115">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="0d11f-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0d11f-116">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="0d11f-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d11f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d11f-117">Requirements</span></span>



| <span data-ttu-id="0d11f-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d11f-118">Requirement</span></span> | <span data-ttu-id="0d11f-119">值</span><span class="sxs-lookup"><span data-stu-id="0d11f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d11f-120">版本</span><span class="sxs-lookup"><span data-stu-id="0d11f-120">Version</span></span><br/> | <span data-ttu-id="0d11f-121">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="0d11f-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="0d11f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0d11f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d11f-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d11f-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d11f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d11f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d11f-125">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="0d11f-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





