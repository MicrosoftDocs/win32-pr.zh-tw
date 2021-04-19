---
title: PlaySound
description: PlaySound 方法會播放指定的音效檔。
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- PlaySound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990638"
---
# <a name="themeplaysound"></a><span data-ttu-id="0149b-104">PlaySound</span><span class="sxs-lookup"><span data-stu-id="0149b-104">THEME.playSound</span></span>

<span data-ttu-id="0149b-105">**PlaySound** 方法會播放指定的音效檔。</span><span class="sxs-lookup"><span data-stu-id="0149b-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="0149b-106">參數</span><span class="sxs-lookup"><span data-stu-id="0149b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0149b-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="0149b-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="0149b-108">**字串**，指定要播放的音效檔名稱。</span><span class="sxs-lookup"><span data-stu-id="0149b-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0149b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0149b-109">Return Value</span></span>

<span data-ttu-id="0149b-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0149b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0149b-111">備註</span><span class="sxs-lookup"><span data-stu-id="0149b-111">Remarks</span></span>

<span data-ttu-id="0149b-112">此方法可讓您將音效效果新增至面板，例如，按一下按鈕時。</span><span class="sxs-lookup"><span data-stu-id="0149b-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="0149b-113">音效是由作業系統直接播放，而不是 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="0149b-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="0149b-114">這表示音效無法利用 Windows Media Player 設定和方法來控制，但可以在 Windows Media Player 播放另一個數位媒體檔案時播放。</span><span class="sxs-lookup"><span data-stu-id="0149b-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="0149b-115">這個方法僅支援 WAV 檔案。</span><span class="sxs-lookup"><span data-stu-id="0149b-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="0149b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0149b-116">Requirements</span></span>



| <span data-ttu-id="0149b-117">需求</span><span class="sxs-lookup"><span data-stu-id="0149b-117">Requirement</span></span> | <span data-ttu-id="0149b-118">值</span><span class="sxs-lookup"><span data-stu-id="0149b-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0149b-119">版本</span><span class="sxs-lookup"><span data-stu-id="0149b-119">Version</span></span><br/> | <span data-ttu-id="0149b-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="0149b-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0149b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0149b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0149b-122">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="0149b-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





