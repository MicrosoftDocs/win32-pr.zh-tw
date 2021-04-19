---
title: Graphicswindow.fontbold 屬性
description: Graphicswindow.fontbold 屬性
ms.assetid: abf735f9-fea2-4d02-a821-e28583a8bc39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6439a7f6b7d6e3bf67620f27c77ce59f8402ce49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976317"
---
# <a name="fontbold-property"></a><span data-ttu-id="e4774-103">Graphicswindow.fontbold 屬性</span><span class="sxs-lookup"><span data-stu-id="e4774-103">FontBold Property</span></span>

<span data-ttu-id="e4774-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e4774-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e4774-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="e4774-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e4774-106">傳回目前在指定字元的 [文字] 氣球視窗中顯示的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="e4774-106">Returns the font style currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="e4774-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="e4774-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e4774-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。Graphicswindow.fontbold**</span><span class="sxs-lookup"><span data-stu-id="e4774-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontBold*\*</span></span>



| <span data-ttu-id="e4774-109">值</span><span class="sxs-lookup"><span data-stu-id="e4774-109">Value</span></span>     | <span data-ttu-id="e4774-110">描述</span><span class="sxs-lookup"><span data-stu-id="e4774-110">Description</span></span>                   |
|-----------|-------------------------------|
| <span data-ttu-id="e4774-111">**True**</span><span class="sxs-lookup"><span data-stu-id="e4774-111">**True**</span></span>  | <span data-ttu-id="e4774-112">提示字元字型為粗體。</span><span class="sxs-lookup"><span data-stu-id="e4774-112">The balloon font is bold.</span></span>     |
| <span data-ttu-id="e4774-113">**False**</span><span class="sxs-lookup"><span data-stu-id="e4774-113">**False**</span></span> | <span data-ttu-id="e4774-114">氣球字型不是粗體。</span><span class="sxs-lookup"><span data-stu-id="e4774-114">The balloon font is not bold.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4774-115">備註</span><span class="sxs-lookup"><span data-stu-id="e4774-115">Remarks</span></span>

<span data-ttu-id="e4774-116">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="e4774-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e4774-117">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="e4774-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




