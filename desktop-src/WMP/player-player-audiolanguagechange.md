---
title: AudioLanguageChange 事件
description: 當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。 |AudioLanguageChange 事件
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- AudioLanguageChange 事件 Windows Media Player
- AudioLanguageChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，AudioLanguageChange 事件
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981119"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="0f606-107">AudioLanguageChange 事件</span><span class="sxs-lookup"><span data-stu-id="0f606-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="0f606-108">當目前的音訊語言變更時，就會發生 **AudioLanguageChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="0f606-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f606-109">語法</span><span class="sxs-lookup"><span data-stu-id="0f606-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="0f606-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f606-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f606-111">*LangID*</span><span class="sxs-lookup"><span data-stu-id="0f606-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="0f606-112"> (**long**) 指定新地區設定識別碼 (LCID) 的 **數位**。</span><span class="sxs-lookup"><span data-stu-id="0f606-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f606-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f606-113">Return value</span></span>

<span data-ttu-id="0f606-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0f606-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f606-115">備註</span><span class="sxs-lookup"><span data-stu-id="0f606-115">Remarks</span></span>

<span data-ttu-id="0f606-116">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="0f606-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="0f606-117">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入的 Microsoft JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="0f606-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="0f606-118">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="0f606-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0f606-119">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0f606-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f606-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f606-120">Requirements</span></span>



| <span data-ttu-id="0f606-121">需求</span><span class="sxs-lookup"><span data-stu-id="0f606-121">Requirement</span></span> | <span data-ttu-id="0f606-122">值</span><span class="sxs-lookup"><span data-stu-id="0f606-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f606-123">版本</span><span class="sxs-lookup"><span data-stu-id="0f606-123">Version</span></span><br/> | <span data-ttu-id="0f606-124">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0f606-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0f606-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f606-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f606-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f606-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f606-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f606-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f606-128">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="0f606-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="0f606-129">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="0f606-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





