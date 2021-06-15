---
title: 'FontSize 屬性 (Balloon 物件) '
description: 瞭解 FontSize Balloon 物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068215"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="f6672-104">FontSize 屬性 (Balloon 物件) </span><span class="sxs-lookup"><span data-stu-id="f6672-104">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="f6672-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f6672-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f6672-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="f6672-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f6672-107">針對指定的字元，傳回或設定文字氣球所支援的字型大小。</span><span class="sxs-lookup"><span data-stu-id="f6672-107">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="f6672-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="f6672-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f6672-109">*agent. \* \* \* 字元* \* **( "**_CharacterID_*_" ) 。FontSize_* \[  =  *點*\]</span><span class="sxs-lookup"><span data-stu-id="f6672-109">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="f6672-110">部分</span><span class="sxs-lookup"><span data-stu-id="f6672-110">Part</span></span>     | <span data-ttu-id="f6672-111">描述</span><span class="sxs-lookup"><span data-stu-id="f6672-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="f6672-112">*點*</span><span class="sxs-lookup"><span data-stu-id="f6672-112">*Points*</span></span> | <span data-ttu-id="f6672-113">長整數值，指定以點為單位的字型大小。</span><span class="sxs-lookup"><span data-stu-id="f6672-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6672-114">備註</span><span class="sxs-lookup"><span data-stu-id="f6672-114">Remarks</span></span>

<span data-ttu-id="f6672-115">[**FontSize**](fontsize-property.md)屬性會傳回長整數值，以點指定目前的字型大小。</span><span class="sxs-lookup"><span data-stu-id="f6672-115">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="f6672-116">**FontSize** 的最大值是2160點。</span><span class="sxs-lookup"><span data-stu-id="f6672-116">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="f6672-117">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="f6672-117">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f6672-118">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="f6672-118">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




