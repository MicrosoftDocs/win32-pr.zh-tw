---
title: PlayMedia 方法
description: 本頁面記載 Windows Media Player 9 系列 SDK 和 Windows Media Player 10 SDK 的功能。 它可能在後續版本中無法使用。
ms.assetid: 48071318-e853-4139-8fe4-17d1cdbef8f5
keywords:
- playMedia 方法 Windows Media Player
- playMedia 方法 Windows Media Player、External 類別
- External class Windows Media Player，playMedia 方法
topic_type:
- apiref
api_name:
- External.playMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0330e7e68d8b4e3747c019e0841f872d279c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984286"
---
# <a name="externalplaymedia-method"></a><span data-ttu-id="a7e50-107">PlayMedia 方法</span><span class="sxs-lookup"><span data-stu-id="a7e50-107">External.playMedia method</span></span>

<span data-ttu-id="a7e50-108">本頁面記載 Windows Media Player 9 系列 SDK 和 Windows Media Player 10 SDK 的功能。</span><span class="sxs-lookup"><span data-stu-id="a7e50-108">This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK.</span></span> <span data-ttu-id="a7e50-109">它可能在後續版本中無法使用。</span><span class="sxs-lookup"><span data-stu-id="a7e50-109">It may be unavailable in subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="a7e50-110">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="a7e50-110">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a7e50-111">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="a7e50-111">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a7e50-112">**PlayMedia** 方法會指定要播放之數位媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="a7e50-112">The **playMedia** method specifies the URL of a digital media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e50-113">語法</span><span class="sxs-lookup"><span data-stu-id="a7e50-113">Syntax</span></span>


```JScript
External.playMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="a7e50-114">參數</span><span class="sxs-lookup"><span data-stu-id="a7e50-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7e50-115">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7e50-115">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e50-116">**字串** ，指定要播放之數位媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="a7e50-116">**String** specifying the URL of the digital media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7e50-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7e50-117">Return value</span></span>

<span data-ttu-id="a7e50-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a7e50-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7e50-119">備註</span><span class="sxs-lookup"><span data-stu-id="a7e50-119">Remarks</span></span>

<span data-ttu-id="a7e50-120">此方法僅適用于 **指南** 功能中裝載的網頁。</span><span class="sxs-lookup"><span data-stu-id="a7e50-120">This method is only available to webpages hosted in the **Guide** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e50-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7e50-121">Requirements</span></span>



| <span data-ttu-id="a7e50-122">需求</span><span class="sxs-lookup"><span data-stu-id="a7e50-122">Requirement</span></span> | <span data-ttu-id="a7e50-123">值</span><span class="sxs-lookup"><span data-stu-id="a7e50-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e50-124">版本</span><span class="sxs-lookup"><span data-stu-id="a7e50-124">Version</span></span><br/> | <span data-ttu-id="a7e50-125">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="a7e50-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a7e50-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a7e50-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a7e50-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7e50-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e50-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7e50-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e50-129">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="a7e50-129">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





