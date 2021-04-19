---
title: SEEKSLIDER
description: 這是具有下列預設值的預先定義滑杆。 |SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978630"
---
# <a name="seekslider"></a><span data-ttu-id="ab4db-105">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="ab4db-105">SEEKSLIDER</span></span>

<span data-ttu-id="ab4db-106">這是具有下列預設值的預先定義 **滑杆** 。</span><span class="sxs-lookup"><span data-stu-id="ab4db-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="ab4db-107">備註</span><span class="sxs-lookup"><span data-stu-id="ab4db-107">Remarks</span></span>

<span data-ttu-id="ab4db-108">這會建立 **滑動** 軸控制項，將媒體檔案搜尋至任何位置。</span><span class="sxs-lookup"><span data-stu-id="ab4db-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="ab4db-109">工具提示已當地語系化。</span><span class="sxs-lookup"><span data-stu-id="ab4db-109">The ToolTips are localized.</span></span> <span data-ttu-id="ab4db-110">此 **滑杆** 的所有屬性都可以藉由明確指定來覆寫。</span><span class="sxs-lookup"><span data-stu-id="ab4db-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab4db-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab4db-111">Requirements</span></span>



| <span data-ttu-id="ab4db-112">需求</span><span class="sxs-lookup"><span data-stu-id="ab4db-112">Requirement</span></span> | <span data-ttu-id="ab4db-113">值</span><span class="sxs-lookup"><span data-stu-id="ab4db-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="ab4db-114">版本</span><span class="sxs-lookup"><span data-stu-id="ab4db-114">Version</span></span><br/> | <span data-ttu-id="ab4db-115">Windows Media Player 7.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ab4db-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab4db-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab4db-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4db-117">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="ab4db-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





