---
title: SaveCurrentViewToLibrary 方法
description: SaveCurrentViewToLibrary 方法會從目前視圖中的媒體專案建立播放清單，並將播放清單儲存在本機文件庫中。
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- saveCurrentViewToLibrary 方法 Windows Media Player
- saveCurrentViewToLibrary 方法 Windows Media Player、External 類別
- External class Windows Media Player，saveCurrentViewToLibrary 方法
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982502"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="ec041-106">SaveCurrentViewToLibrary 方法</span><span class="sxs-lookup"><span data-stu-id="ec041-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="ec041-107">**SaveCurrentViewToLibrary** 方法會從目前視圖中的媒體專案建立播放清單，並將播放清單儲存在本機文件庫中。</span><span class="sxs-lookup"><span data-stu-id="ec041-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec041-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec041-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="ec041-109">參數</span><span class="sxs-lookup"><span data-stu-id="ec041-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec041-110">*FriendlyListName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec041-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec041-111">**字串** ，指定播放清單的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ec041-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="ec041-112">Windows Media Player 在其使用者介面中顯示此名稱。</span><span class="sxs-lookup"><span data-stu-id="ec041-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="ec041-113">*本機* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec041-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec041-114">指定播放清單為動態或靜態的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="ec041-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="ec041-115">**TRUE** 指定動態，而 **FALSE** 指定靜態。</span><span class="sxs-lookup"><span data-stu-id="ec041-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec041-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec041-116">Return value</span></span>

<span data-ttu-id="ec041-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec041-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec041-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec041-118">Requirements</span></span>



| <span data-ttu-id="ec041-119">需求</span><span class="sxs-lookup"><span data-stu-id="ec041-119">Requirement</span></span> | <span data-ttu-id="ec041-120">值</span><span class="sxs-lookup"><span data-stu-id="ec041-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec041-121">版本</span><span class="sxs-lookup"><span data-stu-id="ec041-121">Version</span></span><br/> | <span data-ttu-id="ec041-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ec041-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="ec041-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ec041-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec041-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec041-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec041-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec041-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec041-126">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="ec041-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





