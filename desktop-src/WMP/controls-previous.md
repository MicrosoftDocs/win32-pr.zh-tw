---
title: Controls。 previous 方法
description: 先前的方法會將目前的專案設定為播放清單中的上一個專案。
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- 上一個方法 Windows Media Player
- 上一個方法 Windows Media Player，Controls 類別
- 控制項類別 Windows Media Player、上一個方法
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981306"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="2f019-106">Controls。 previous 方法</span><span class="sxs-lookup"><span data-stu-id="2f019-106">Controls.previous method</span></span>

<span data-ttu-id="2f019-107">**先前** 的方法會將目前的專案設定為播放清單中的上一個專案。</span><span class="sxs-lookup"><span data-stu-id="2f019-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f019-108">語法</span><span class="sxs-lookup"><span data-stu-id="2f019-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="2f019-109">參數</span><span class="sxs-lookup"><span data-stu-id="2f019-109">Parameters</span></span>

<span data-ttu-id="2f019-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2f019-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f019-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f019-111">Return value</span></span>

<span data-ttu-id="2f019-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2f019-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f019-113">備註</span><span class="sxs-lookup"><span data-stu-id="2f019-113">Remarks</span></span>

<span data-ttu-id="2f019-114">如果播放清單是在叫用 **先前** 的第一個專案時，播放清單中的最後一個專案會成為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="2f019-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="2f019-115">範例</span><span class="sxs-lookup"><span data-stu-id="2f019-115">Examples</span></span>

<span data-ttu-id="2f019-116">下列範例會建立 HTML BUTTON 專案，使用 [ **上一步** ] 移至目前播放清單中的上一個專案。</span><span class="sxs-lookup"><span data-stu-id="2f019-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="2f019-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f019-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="2f019-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f019-118">Requirements</span></span>



| <span data-ttu-id="2f019-119">需求</span><span class="sxs-lookup"><span data-stu-id="2f019-119">Requirement</span></span> | <span data-ttu-id="2f019-120">值</span><span class="sxs-lookup"><span data-stu-id="2f019-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f019-121">版本</span><span class="sxs-lookup"><span data-stu-id="2f019-121">Version</span></span><br/> | <span data-ttu-id="2f019-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2f019-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2f019-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2f019-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f019-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f019-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f019-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f019-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f019-126">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="2f019-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="2f019-127">**控制項。下一步**</span><span class="sxs-lookup"><span data-stu-id="2f019-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="2f019-128">**控制項。停止**</span><span class="sxs-lookup"><span data-stu-id="2f019-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





