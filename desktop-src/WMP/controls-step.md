---
title: Controls 方法
description: Step 方法會導致目前的影片媒體專案凍結下一個畫面或上一個畫面格的播放。
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- 步驟方法 Windows Media Player
- 步驟方法 Windows Media Player、控制項類別
- Controls 類別 Windows Media Player、step 方法
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001818"
---
# <a name="controlsstep-method"></a><span data-ttu-id="d92e4-106">Controls 方法</span><span class="sxs-lookup"><span data-stu-id="d92e4-106">Controls.step method</span></span>

<span data-ttu-id="d92e4-107">**Step** 方法會導致目前的影片媒體專案凍結下一個畫面或上一個畫面格的播放。</span><span class="sxs-lookup"><span data-stu-id="d92e4-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92e4-108">語法</span><span class="sxs-lookup"><span data-stu-id="d92e4-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="d92e4-109">參數</span><span class="sxs-lookup"><span data-stu-id="d92e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d92e4-110">*frameCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d92e4-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92e4-111">**Number** (**long**) 指出凍結前要執行的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="d92e4-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="d92e4-112">目前必須設定為1或-1。</span><span class="sxs-lookup"><span data-stu-id="d92e4-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d92e4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d92e4-113">Return value</span></span>

<span data-ttu-id="d92e4-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d92e4-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92e4-115">備註</span><span class="sxs-lookup"><span data-stu-id="d92e4-115">Remarks</span></span>

<span data-ttu-id="d92e4-116">這個方法目前僅支援參數1或-1，因此您一次只能執行一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="d92e4-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="d92e4-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d92e4-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92e4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d92e4-118">Requirements</span></span>



| <span data-ttu-id="d92e4-119">需求</span><span class="sxs-lookup"><span data-stu-id="d92e4-119">Requirement</span></span> | <span data-ttu-id="d92e4-120">值</span><span class="sxs-lookup"><span data-stu-id="d92e4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d92e4-121">版本</span><span class="sxs-lookup"><span data-stu-id="d92e4-121">Version</span></span><br/> | <span data-ttu-id="d92e4-122">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="d92e4-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="d92e4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d92e4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d92e4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d92e4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92e4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d92e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92e4-126">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="d92e4-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="d92e4-127">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="d92e4-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





