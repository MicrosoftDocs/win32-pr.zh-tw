---
title: 播放清單。複製
description: 複製方法會從 CD 開始複製作業。
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- 播放清單。複製 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994291"
---
# <a name="playlistcopy"></a><span data-ttu-id="c41bc-104">播放清單。複製</span><span class="sxs-lookup"><span data-stu-id="c41bc-104">PLAYLIST.copy</span></span>

<span data-ttu-id="c41bc-105">**複製** 方法會從 CD 開始複製作業。</span><span class="sxs-lookup"><span data-stu-id="c41bc-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="c41bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="c41bc-106">Parameters</span></span>

<span data-ttu-id="c41bc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c41bc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c41bc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c41bc-108">Return Value</span></span>

<span data-ttu-id="c41bc-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c41bc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c41bc-110">備註</span><span class="sxs-lookup"><span data-stu-id="c41bc-110">Remarks</span></span>

<span data-ttu-id="c41bc-111">這個方法只會複製播放清單中的已核取專案，而且其運作方式與在 Windows Media Player 的完整模式中， **從 [從 CD 複製** ] 窗格的方式相同。</span><span class="sxs-lookup"><span data-stu-id="c41bc-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="c41bc-112">若要讓此方法運作，cd 必須位於 CD 光碟機中。</span><span class="sxs-lookup"><span data-stu-id="c41bc-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="c41bc-113">將 **checkboxesVisible** 屬性設定為 true，可讓使用者在複製前選取 CD 上的個別專案。</span><span class="sxs-lookup"><span data-stu-id="c41bc-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="c41bc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c41bc-114">Requirements</span></span>



| <span data-ttu-id="c41bc-115">需求</span><span class="sxs-lookup"><span data-stu-id="c41bc-115">Requirement</span></span> | <span data-ttu-id="c41bc-116">值</span><span class="sxs-lookup"><span data-stu-id="c41bc-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c41bc-117">版本</span><span class="sxs-lookup"><span data-stu-id="c41bc-117">Version</span></span><br/> | <span data-ttu-id="c41bc-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c41bc-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c41bc-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c41bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41bc-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="c41bc-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="c41bc-121">**播放清單。 abortCopy**</span><span class="sxs-lookup"><span data-stu-id="c41bc-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="c41bc-122">**播放清單。複製**</span><span class="sxs-lookup"><span data-stu-id="c41bc-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





