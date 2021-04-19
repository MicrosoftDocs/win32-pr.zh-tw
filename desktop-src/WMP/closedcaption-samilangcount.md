---
title: ClosedCaption.SAMILangCount
description: SAMILangCount 屬性會抓取目前的薩米文檔案所支援的語言數目。
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- ClosedCaption. SAMILangCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992569"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="fd3ea-104">ClosedCaption.SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="fd3ea-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="fd3ea-105">**SAMILangCount** 屬性會抓取目前的薩米文檔案所支援的語言數目。</span><span class="sxs-lookup"><span data-stu-id="fd3ea-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="fd3ea-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="fd3ea-106">Possible Values</span></span>

<span data-ttu-id="fd3ea-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="fd3ea-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3ea-108">備註</span><span class="sxs-lookup"><span data-stu-id="fd3ea-108">Remarks</span></span>

<span data-ttu-id="fd3ea-109">在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。</span><span class="sxs-lookup"><span data-stu-id="fd3ea-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="fd3ea-110">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。</span><span class="sxs-lookup"><span data-stu-id="fd3ea-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3ea-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd3ea-111">Requirements</span></span>



| <span data-ttu-id="fd3ea-112">需求</span><span class="sxs-lookup"><span data-stu-id="fd3ea-112">Requirement</span></span> | <span data-ttu-id="fd3ea-113">值</span><span class="sxs-lookup"><span data-stu-id="fd3ea-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3ea-114">版本</span><span class="sxs-lookup"><span data-stu-id="fd3ea-114">Version</span></span><br/> | <span data-ttu-id="fd3ea-115">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="fd3ea-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fd3ea-116">DLL</span><span class="sxs-lookup"><span data-stu-id="fd3ea-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd3ea-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd3ea-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3ea-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd3ea-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3ea-119">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="fd3ea-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="fd3ea-120">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="fd3ea-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="fd3ea-121">**ClosedCaption.getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="fd3ea-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="fd3ea-122">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="fd3ea-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





