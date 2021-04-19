---
title: External. play 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Play 方法會指示 Windows Media Player 播放一組媒體專案。
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- play 方法 Windows Media Player
- play 方法 Windows Media Player、External 類別
- 外部類別 Windows Media Player、play 方法
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992787"
---
# <a name="externalplay-method"></a><span data-ttu-id="bb286-108">External. play 方法</span><span class="sxs-lookup"><span data-stu-id="bb286-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="bb286-109">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="bb286-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bb286-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="bb286-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bb286-111">**Play** 方法會指示 Windows Media Player 播放一組媒體專案。</span><span class="sxs-lookup"><span data-stu-id="bb286-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb286-112">語法</span><span class="sxs-lookup"><span data-stu-id="bb286-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="bb286-113">參數</span><span class="sxs-lookup"><span data-stu-id="bb286-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb286-114">*LibraryLocationType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb286-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb286-115">連結 [庫位置常數](library-location-constants.md) ，指定要播放之媒體專案的型別。</span><span class="sxs-lookup"><span data-stu-id="bb286-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="bb286-116">例如，CPAlbumID 指定要播放一或多個專輯。</span><span class="sxs-lookup"><span data-stu-id="bb286-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="bb286-117">*LibraryLocationIDs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb286-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb286-118">**字串** ，包含要播放之媒體專案的識別碼（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="bb286-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb286-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb286-119">Return value</span></span>

<span data-ttu-id="bb286-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bb286-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb286-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb286-121">Requirements</span></span>



| <span data-ttu-id="bb286-122">需求</span><span class="sxs-lookup"><span data-stu-id="bb286-122">Requirement</span></span> | <span data-ttu-id="bb286-123">值</span><span class="sxs-lookup"><span data-stu-id="bb286-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb286-124">版本</span><span class="sxs-lookup"><span data-stu-id="bb286-124">Version</span></span><br/> | <span data-ttu-id="bb286-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="bb286-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="bb286-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb286-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb286-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb286-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb286-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb286-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb286-129">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="bb286-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





