---
title: 'FontSize 屬性 (Balloon 物件) '
description: FontSize 屬性
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383722"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="daa45-103">FontSize 屬性 (Balloon 物件) </span><span class="sxs-lookup"><span data-stu-id="daa45-103">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="daa45-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="daa45-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="daa45-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="daa45-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="daa45-106">針對指定的字元，傳回或設定文字氣球所支援的字型大小。</span><span class="sxs-lookup"><span data-stu-id="daa45-106">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="daa45-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="daa45-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="daa45-108">*agent. \* \* \* 字元* \* **( "**_CharacterID_*_" ) 。FontSize_* \[  =  *點*\]</span><span class="sxs-lookup"><span data-stu-id="daa45-108">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="daa45-109">部分</span><span class="sxs-lookup"><span data-stu-id="daa45-109">Part</span></span>     | <span data-ttu-id="daa45-110">描述</span><span class="sxs-lookup"><span data-stu-id="daa45-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="daa45-111">*點*</span><span class="sxs-lookup"><span data-stu-id="daa45-111">*Points*</span></span> | <span data-ttu-id="daa45-112">長整數值，指定以點為單位的字型大小。</span><span class="sxs-lookup"><span data-stu-id="daa45-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daa45-113">備註</span><span class="sxs-lookup"><span data-stu-id="daa45-113">Remarks</span></span>

<span data-ttu-id="daa45-114">[**FontSize**](fontsize-property.md)屬性會傳回長整數值，以點指定目前的字型大小。</span><span class="sxs-lookup"><span data-stu-id="daa45-114">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="daa45-115">**FontSize** 的最大值是2160點。</span><span class="sxs-lookup"><span data-stu-id="daa45-115">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="daa45-116">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="daa45-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="daa45-117">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="daa45-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




