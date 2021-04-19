---
title: Controls. next 方法
description: 下一個方法會將目前的專案設定為播放清單中的下一個專案。
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- next 方法 Windows Media Player
- next 方法 Windows Media Player，Controls 類別
- 控制項類別 Windows Media Player、next 方法
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983232"
---
# <a name="controlsnext-method"></a><span data-ttu-id="2bd5c-106">Controls. next 方法</span><span class="sxs-lookup"><span data-stu-id="2bd5c-106">Controls.next method</span></span>

<span data-ttu-id="2bd5c-107">**下一個** 方法會將目前的專案設定為播放清單中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd5c-108">語法</span><span class="sxs-lookup"><span data-stu-id="2bd5c-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="2bd5c-109">參數</span><span class="sxs-lookup"><span data-stu-id="2bd5c-109">Parameters</span></span>

<span data-ttu-id="2bd5c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bd5c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bd5c-111">Return value</span></span>

<span data-ttu-id="2bd5c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd5c-113">備註</span><span class="sxs-lookup"><span data-stu-id="2bd5c-113">Remarks</span></span>

<span data-ttu-id="2bd5c-114">如果叫用 [ **下一步]** 時，播放清單是最後一個專案，播放清單中的第一個專案就會成為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="2bd5c-115">針對伺服器端播放清單，這個方法會跳至伺服器端播放清單中的下一個專案，而不是用戶端播放清單。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="2bd5c-116">播放 DVD 時，此方法會跳到播放順序中的下一個邏輯章節，這可能不是播放清單中的下一章。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="2bd5c-117">播放 DVD 靜止時，此方法會跳到下一個仍然的。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="2bd5c-118">範例</span><span class="sxs-lookup"><span data-stu-id="2bd5c-118">Examples</span></span>

<span data-ttu-id="2bd5c-119">下列範例會建立 HTML BUTTON 專案，使用 **[下一步]** 移至目前播放清單中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="2bd5c-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="2bd5c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bd5c-121">Requirements</span></span>



| <span data-ttu-id="2bd5c-122">需求</span><span class="sxs-lookup"><span data-stu-id="2bd5c-122">Requirement</span></span> | <span data-ttu-id="2bd5c-123">值</span><span class="sxs-lookup"><span data-stu-id="2bd5c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd5c-124">版本</span><span class="sxs-lookup"><span data-stu-id="2bd5c-124">Version</span></span><br/> | <span data-ttu-id="2bd5c-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2bd5c-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2bd5c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd5c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="2bd5c-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd5c-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd5c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bd5c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd5c-129">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="2bd5c-130">**控制項。上一個**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="2bd5c-131">**控制項。停止**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





