---
title: FontUnderline 屬性
description: FontUnderline 屬性
ms.assetid: 6fe6c147-2969-470e-9742-da2e6b3614e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970986ee9159df2f36bc99e91ace21146693073a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021032"
---
# <a name="fontunderline-property"></a><span data-ttu-id="2cb66-103">FontUnderline 屬性</span><span class="sxs-lookup"><span data-stu-id="2cb66-103">FontUnderline Property</span></span>

<span data-ttu-id="2cb66-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2cb66-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2cb66-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2cb66-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2cb66-106">傳回目前在指定字元的 [文字] 氣球視窗中顯示的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="2cb66-106">Returns the font style currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="2cb66-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2cb66-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2cb66-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。FontUnderline**</span><span class="sxs-lookup"><span data-stu-id="2cb66-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontUnderline*\*</span></span>



| <span data-ttu-id="2cb66-109">值</span><span class="sxs-lookup"><span data-stu-id="2cb66-109">Value</span></span>     | <span data-ttu-id="2cb66-110">描述</span><span class="sxs-lookup"><span data-stu-id="2cb66-110">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="2cb66-111">**True**</span><span class="sxs-lookup"><span data-stu-id="2cb66-111">**True**</span></span>  | <span data-ttu-id="2cb66-112">批註提示字型會加上底線。</span><span class="sxs-lookup"><span data-stu-id="2cb66-112">The balloon font is underlined.</span></span>     |
| <span data-ttu-id="2cb66-113">**False**</span><span class="sxs-lookup"><span data-stu-id="2cb66-113">**False**</span></span> | <span data-ttu-id="2cb66-114">提示字元字型未加上底線。</span><span class="sxs-lookup"><span data-stu-id="2cb66-114">The balloon font is not underlined.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cb66-115">備註</span><span class="sxs-lookup"><span data-stu-id="2cb66-115">Remarks</span></span>

<span data-ttu-id="2cb66-116">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="2cb66-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2cb66-117">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="2cb66-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




