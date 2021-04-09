---
title: 大小事件
description: 大小事件
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839867"
---
# <a name="size-event"></a><span data-ttu-id="c8291-103">大小事件</span><span class="sxs-lookup"><span data-stu-id="c8291-103">Size Event</span></span>

<span data-ttu-id="c8291-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c8291-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c8291-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="c8291-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c8291-106">發生于字元的大小變更時。</span><span class="sxs-lookup"><span data-stu-id="c8291-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="c8291-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="c8291-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c8291-108">\**子\*\*\*代理程式* \_ **大小 (byval** *CharacterID*， **byval** *寬度*， **byval** *高度*) </span><span class="sxs-lookup"><span data-stu-id="c8291-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="c8291-109">部分</span><span class="sxs-lookup"><span data-stu-id="c8291-109">Part</span></span>          | <span data-ttu-id="c8291-110">描述</span><span class="sxs-lookup"><span data-stu-id="c8291-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="c8291-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="c8291-111">*CharacterID*</span></span> | <span data-ttu-id="c8291-112">傳回已移動之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8291-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="c8291-113">*寬度*</span><span class="sxs-lookup"><span data-stu-id="c8291-113">*Width*</span></span>       | <span data-ttu-id="c8291-114">傳回字元框架的新寬度 (以圖元為單位) 為整數。</span><span class="sxs-lookup"><span data-stu-id="c8291-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="c8291-115">*高度*</span><span class="sxs-lookup"><span data-stu-id="c8291-115">*Height*</span></span>      | <span data-ttu-id="c8291-116">傳回字元框架的新高度 (以圖元為單位) 為整數。</span><span class="sxs-lookup"><span data-stu-id="c8291-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="c8291-117">備註</span><span class="sxs-lookup"><span data-stu-id="c8291-117">Remarks</span></span>

<span data-ttu-id="c8291-118">當應用程式變更字元的大小時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="c8291-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="c8291-119">此事件只會傳送給已載入字元)  (應用程式的字元用戶端。</span><span class="sxs-lookup"><span data-stu-id="c8291-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="c8291-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8291-120">See Also</span></span>

[<span data-ttu-id="c8291-121">**移動事件**</span><span class="sxs-lookup"><span data-stu-id="c8291-121">**Move event**</span></span>](move-event.md)


 

 




