---
title: DefaultCharacterChange 事件
description: DefaultCharacterChange 事件
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372384"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="378c4-103">DefaultCharacterChange 事件</span><span class="sxs-lookup"><span data-stu-id="378c4-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="378c4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="378c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="378c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="378c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="378c4-106">當使用者變更預設字元時發生。</span><span class="sxs-lookup"><span data-stu-id="378c4-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="378c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="378c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="378c4-108">**子\*\*\*代理程式。 \* \* \* DefaultCharacterChange* \*  **(ByVal** *GUID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="378c4-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="378c4-109">部分</span><span class="sxs-lookup"><span data-stu-id="378c4-109">Part</span></span>   | <span data-ttu-id="378c4-110">描述</span><span class="sxs-lookup"><span data-stu-id="378c4-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="378c4-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="378c4-111">*GUID*</span></span> | <span data-ttu-id="378c4-112">傳回字元的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="378c4-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="378c4-113">備註</span><span class="sxs-lookup"><span data-stu-id="378c4-113">Remarks</span></span>

<span data-ttu-id="378c4-114">此事件表示使用者已變更指派為使用者預設字元的字元。</span><span class="sxs-lookup"><span data-stu-id="378c4-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="378c4-115">伺服器只將此傳送給已載入預設字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="378c4-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="378c4-116">出現新的字元時，它會假設與任何已載入的字元實例或先前的預設字元相同的大小，) 的順序 (。</span><span class="sxs-lookup"><span data-stu-id="378c4-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="378c4-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="378c4-117">See Also</span></span>

<span data-ttu-id="378c4-118">[**ShowDefaultCharacterProperties 方法**](showdefaultcharacterproperties-method.md)， [ **Load 方法**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="378c4-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




