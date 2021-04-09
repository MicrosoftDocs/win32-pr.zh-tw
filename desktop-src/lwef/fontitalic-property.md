---
title: FontItalic 屬性
description: FontItalic 屬性
ms.assetid: fa34c2ca-b200-435f-8191-3ad5b33fe2b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007fdb30f3f751a8cd410a07bd8bcefa17524ff6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671864"
---
# <a name="fontitalic-property"></a><span data-ttu-id="9bc51-103">FontItalic 屬性</span><span class="sxs-lookup"><span data-stu-id="9bc51-103">FontItalic Property</span></span>

<span data-ttu-id="9bc51-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9bc51-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9bc51-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="9bc51-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9bc51-106">傳回目前在指定字元的 [文字] 氣球視窗中顯示的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="9bc51-106">Returns the font style currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9bc51-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="9bc51-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9bc51-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。FontItalic**</span><span class="sxs-lookup"><span data-stu-id="9bc51-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontItalic*\*</span></span>



| <span data-ttu-id="9bc51-109">值</span><span class="sxs-lookup"><span data-stu-id="9bc51-109">Value</span></span>     | <span data-ttu-id="9bc51-110">描述</span><span class="sxs-lookup"><span data-stu-id="9bc51-110">Description</span></span>                     |
|-----------|---------------------------------|
| <span data-ttu-id="9bc51-111">**True**</span><span class="sxs-lookup"><span data-stu-id="9bc51-111">**True**</span></span>  | <span data-ttu-id="9bc51-112">氣球字型為斜體。</span><span class="sxs-lookup"><span data-stu-id="9bc51-112">The balloon font is italic.</span></span>     |
| <span data-ttu-id="9bc51-113">**False**</span><span class="sxs-lookup"><span data-stu-id="9bc51-113">**False**</span></span> | <span data-ttu-id="9bc51-114">氣球字型不是斜體。</span><span class="sxs-lookup"><span data-stu-id="9bc51-114">The balloon font is not italic.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bc51-115">備註</span><span class="sxs-lookup"><span data-stu-id="9bc51-115">Remarks</span></span>

<span data-ttu-id="9bc51-116">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="9bc51-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9bc51-117">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="9bc51-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




