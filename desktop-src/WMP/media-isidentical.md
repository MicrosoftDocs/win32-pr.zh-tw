---
title: IsIdentical 方法
description: IsIdentical 方法會抓取值，指出提供的物件是否與目前的物件相同。 |IsIdentical 方法
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999268"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="40c89-107">IsIdentical 方法</span><span class="sxs-lookup"><span data-stu-id="40c89-107">Media.isIdentical method</span></span>

<span data-ttu-id="40c89-108">**IsIdentical** 方法會抓取值，指出提供的物件是否與目前的物件相同。</span><span class="sxs-lookup"><span data-stu-id="40c89-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c89-109">語法</span><span class="sxs-lookup"><span data-stu-id="40c89-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="40c89-110">參數</span><span class="sxs-lookup"><span data-stu-id="40c89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c89-111">*媒體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40c89-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c89-112">要與目前 **媒體** 物件比較的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="40c89-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c89-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="40c89-113">Return value</span></span>

<span data-ttu-id="40c89-114">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="40c89-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="40c89-115">範例</span><span class="sxs-lookup"><span data-stu-id="40c89-115">Examples</span></span>

<span data-ttu-id="40c89-116">下列 JScript 範例會使用 *媒體*。**isIdentical** ，檢查名為 newMedia 的媒體專案是否與目前的媒體專案相同。</span><span class="sxs-lookup"><span data-stu-id="40c89-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="40c89-117">如果兩者不同，則會播放新的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="40c89-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="40c89-118">否則，目前的媒體會繼續播放不中斷的。</span><span class="sxs-lookup"><span data-stu-id="40c89-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="40c89-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="40c89-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="40c89-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="40c89-120">Requirements</span></span>



| <span data-ttu-id="40c89-121">需求</span><span class="sxs-lookup"><span data-stu-id="40c89-121">Requirement</span></span> | <span data-ttu-id="40c89-122">值</span><span class="sxs-lookup"><span data-stu-id="40c89-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40c89-123">版本</span><span class="sxs-lookup"><span data-stu-id="40c89-123">Version</span></span><br/> | <span data-ttu-id="40c89-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="40c89-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="40c89-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40c89-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="40c89-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40c89-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c89-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40c89-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c89-128">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="40c89-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





