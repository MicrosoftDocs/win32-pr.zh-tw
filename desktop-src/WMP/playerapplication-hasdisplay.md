---
title: PlayerApplication.hasDisplay
description: HasDisplay 屬性會抓取值，指出影片是否可以透過遠端播放機控制項來顯示。
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000767"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="65249-104">PlayerApplication.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="65249-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="65249-105">**HasDisplay** 屬性會抓取值，指出影片是否可以透過遠端播放機控制項來顯示。</span><span class="sxs-lookup"><span data-stu-id="65249-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="65249-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="65249-106">Syntax</span></span>

<span data-ttu-id="65249-107">*playerApplication*。**hasDisplay**</span><span class="sxs-lookup"><span data-stu-id="65249-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="65249-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="65249-108">Possible Values</span></span>

<span data-ttu-id="65249-109">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="65249-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="65249-110">備註</span><span class="sxs-lookup"><span data-stu-id="65249-110">Remarks</span></span>

<span data-ttu-id="65249-111">只有在遠端處理 Windows Media Player 控制項時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="65249-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="65249-112">您可以同時在遠端執行數個 Windows Media Player 控制項，但在播放程式的完整模式或其中一個遠端 Windows Media Player 控制項中，影片一次只能顯示在一個位置。</span><span class="sxs-lookup"><span data-stu-id="65249-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="65249-113">您可以使用這個屬性來判斷目前的控制項是否為可顯示影片的控制項。</span><span class="sxs-lookup"><span data-stu-id="65249-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="65249-114">**Windows Media Player 10** 行動裝置版：這個屬性一律會傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="65249-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65249-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="65249-115">Requirements</span></span>



| <span data-ttu-id="65249-116">需求</span><span class="sxs-lookup"><span data-stu-id="65249-116">Requirement</span></span> | <span data-ttu-id="65249-117">值</span><span class="sxs-lookup"><span data-stu-id="65249-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65249-118">版本</span><span class="sxs-lookup"><span data-stu-id="65249-118">Version</span></span><br/> | <span data-ttu-id="65249-119">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="65249-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="65249-120">DLL</span><span class="sxs-lookup"><span data-stu-id="65249-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="65249-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65249-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65249-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65249-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65249-123">**PlayerApplication 物件**</span><span class="sxs-lookup"><span data-stu-id="65249-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="65249-124">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="65249-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





