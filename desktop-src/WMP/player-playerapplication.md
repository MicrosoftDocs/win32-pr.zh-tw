---
title: PlayerApplication
description: 當遠端 Windows Media Player 控制項正在執行時，playerApplication 屬性會捕獲 PlayerApplication 物件。
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- PlayerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994682"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="7383b-104">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="7383b-104">Player.playerApplication</span></span>

<span data-ttu-id="7383b-105">當遠端 Windows Media Player 控制項正在執行時， **playerApplication** 屬性會捕獲 **playerApplication** 物件。</span><span class="sxs-lookup"><span data-stu-id="7383b-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="7383b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7383b-106">Syntax</span></span>

<span data-ttu-id="7383b-107">**playerApplication**</span><span class="sxs-lookup"><span data-stu-id="7383b-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7383b-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="7383b-108">Possible Values</span></span>

<span data-ttu-id="7383b-109">這個屬性是唯讀 **PlayerApplication** 物件或 null 值。</span><span class="sxs-lookup"><span data-stu-id="7383b-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7383b-110">備註</span><span class="sxs-lookup"><span data-stu-id="7383b-110">Remarks</span></span>

<span data-ttu-id="7383b-111">只有在遠端處理 Windows Media Playercontrol 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7383b-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="7383b-112">如果值為 null，則不會在遠端模式中內嵌 Windows Media Playercontrol。</span><span class="sxs-lookup"><span data-stu-id="7383b-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="7383b-113">這個屬性只能在 c + + 程式碼中存取，或透過 playerApplication 全域變數在外觀的腳本中存取。</span><span class="sxs-lookup"><span data-stu-id="7383b-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7383b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7383b-114">Requirements</span></span>



| <span data-ttu-id="7383b-115">需求</span><span class="sxs-lookup"><span data-stu-id="7383b-115">Requirement</span></span> | <span data-ttu-id="7383b-116">值</span><span class="sxs-lookup"><span data-stu-id="7383b-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7383b-117">版本</span><span class="sxs-lookup"><span data-stu-id="7383b-117">Version</span></span><br/> | <span data-ttu-id="7383b-118">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="7383b-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7383b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7383b-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="7383b-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7383b-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7383b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7383b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7383b-122">**全域屬性**</span><span class="sxs-lookup"><span data-stu-id="7383b-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="7383b-123">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="7383b-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7383b-124">**PlayerApplication 物件**</span><span class="sxs-lookup"><span data-stu-id="7383b-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="7383b-125">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="7383b-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





