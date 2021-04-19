---
title: 'FontSize 屬性 (命令物件) '
description: FontSize 屬性
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106984950"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="7dd55-103">FontSize 屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="7dd55-103">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="7dd55-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7dd55-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7dd55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="7dd55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7dd55-106">傳回或設定在字元的快顯功能表中使用的字型大小。</span><span class="sxs-lookup"><span data-stu-id="7dd55-106">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="7dd55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="7dd55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7dd55-108">\*agent. \***字元 ( "**_CharacterID_\*_" ) . FontSize_ \*  \[  =  *點*\]</span><span class="sxs-lookup"><span data-stu-id="7dd55-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="7dd55-109">部分</span><span class="sxs-lookup"><span data-stu-id="7dd55-109">Part</span></span>     | <span data-ttu-id="7dd55-110">描述</span><span class="sxs-lookup"><span data-stu-id="7dd55-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="7dd55-111">*點*</span><span class="sxs-lookup"><span data-stu-id="7dd55-111">*Points*</span></span> | <span data-ttu-id="7dd55-112">長整數值，指定以點為單位的字型大小。</span><span class="sxs-lookup"><span data-stu-id="7dd55-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7dd55-113">備註</span><span class="sxs-lookup"><span data-stu-id="7dd55-113">Remarks</span></span>

<span data-ttu-id="7dd55-114">**FontSize** 屬性會定義用來在字元的快顯功能表中顯示文字的字型的點大小。</span><span class="sxs-lookup"><span data-stu-id="7dd55-114">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="7dd55-115">字型設定的預設值是以字元 **LanguageID** 設定的功能表字型設定為基礎，或者，如果未設定，則是使用者預設語言設定。</span><span class="sxs-lookup"><span data-stu-id="7dd55-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="7dd55-116">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="7dd55-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




