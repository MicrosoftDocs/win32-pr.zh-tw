---
title: PlayerApplication.playerDocked
description: PlayerDocked 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。
ms.assetid: c6f82188-0826-4854-992c-85ad84701fb7
keywords:
- PlayerApplication. playerDocked Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.playerDocked
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c53ac92aac82c19dd9e58d389dee340a5951457b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979439"
---
# <a name="playerapplicationplayerdocked"></a><span data-ttu-id="18cf7-104">PlayerApplication.playerDocked</span><span class="sxs-lookup"><span data-stu-id="18cf7-104">PlayerApplication.playerDocked</span></span>

<span data-ttu-id="18cf7-105">**PlayerDocked** 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。</span><span class="sxs-lookup"><span data-stu-id="18cf7-105">The **playerDocked** property retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>

## <a name="syntax"></a><span data-ttu-id="18cf7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="18cf7-106">Syntax</span></span>

<span data-ttu-id="18cf7-107">*playerApplication*。**playerDocked**</span><span class="sxs-lookup"><span data-stu-id="18cf7-107">*playerApplication*.**playerDocked**</span></span>

## <a name="possible-values"></a><span data-ttu-id="18cf7-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="18cf7-108">Possible Values</span></span>

<span data-ttu-id="18cf7-109">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="18cf7-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="18cf7-110">備註</span><span class="sxs-lookup"><span data-stu-id="18cf7-110">Remarks</span></span>

<span data-ttu-id="18cf7-111">只有在遠端處理 Windows Media Player 控制項時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="18cf7-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="18cf7-112">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="18cf7-112">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18cf7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="18cf7-113">Requirements</span></span>



| <span data-ttu-id="18cf7-114">需求</span><span class="sxs-lookup"><span data-stu-id="18cf7-114">Requirement</span></span> | <span data-ttu-id="18cf7-115">值</span><span class="sxs-lookup"><span data-stu-id="18cf7-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18cf7-116">版本</span><span class="sxs-lookup"><span data-stu-id="18cf7-116">Version</span></span><br/> | <span data-ttu-id="18cf7-117">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="18cf7-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="18cf7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="18cf7-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="18cf7-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18cf7-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18cf7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18cf7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18cf7-121">**PlayerApplication 物件**</span><span class="sxs-lookup"><span data-stu-id="18cf7-121">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="18cf7-122">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="18cf7-122">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





