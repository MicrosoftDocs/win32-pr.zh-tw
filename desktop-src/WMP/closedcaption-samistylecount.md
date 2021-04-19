---
title: ClosedCaption.SAMIStyleCount
description: SAMIStyleCount 屬性會抓取目前的薩米文檔案所支援的樣式數目。
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption. SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999103"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="285a6-104">ClosedCaption.SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="285a6-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="285a6-105">**SAMIStyleCount** 屬性會抓取目前的薩米文檔案所支援的樣式數目。</span><span class="sxs-lookup"><span data-stu-id="285a6-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="285a6-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="285a6-106">Possible Values</span></span>

<span data-ttu-id="285a6-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="285a6-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="285a6-108">備註</span><span class="sxs-lookup"><span data-stu-id="285a6-108">Remarks</span></span>

<span data-ttu-id="285a6-109">在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。</span><span class="sxs-lookup"><span data-stu-id="285a6-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="285a6-110">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。</span><span class="sxs-lookup"><span data-stu-id="285a6-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="285a6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="285a6-111">Requirements</span></span>



| <span data-ttu-id="285a6-112">需求</span><span class="sxs-lookup"><span data-stu-id="285a6-112">Requirement</span></span> | <span data-ttu-id="285a6-113">值</span><span class="sxs-lookup"><span data-stu-id="285a6-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="285a6-114">版本</span><span class="sxs-lookup"><span data-stu-id="285a6-114">Version</span></span><br/> | <span data-ttu-id="285a6-115">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="285a6-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="285a6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="285a6-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="285a6-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="285a6-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285a6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="285a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285a6-119">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="285a6-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="285a6-120">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="285a6-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="285a6-121">**ClosedCaption.getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="285a6-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="285a6-122">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="285a6-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





