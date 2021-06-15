---
title: 'FontName 屬性 (命令物件) '
description: 瞭解 FontName 命令物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068254"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="9d659-104">FontName 屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="9d659-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="9d659-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9d659-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9d659-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="9d659-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9d659-107">傳回或設定在字元的快顯功能表中使用的字型。</span><span class="sxs-lookup"><span data-stu-id="9d659-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="9d659-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="9d659-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9d659-109">\*agent. \***字元 ( "**_CharacterID_\*_" ) . FontName_ \*  \[  =  *字型*\]</span><span class="sxs-lookup"><span data-stu-id="9d659-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="9d659-110">部分</span><span class="sxs-lookup"><span data-stu-id="9d659-110">Part</span></span>   | <span data-ttu-id="9d659-111">描述</span><span class="sxs-lookup"><span data-stu-id="9d659-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="9d659-112">*字型*</span><span class="sxs-lookup"><span data-stu-id="9d659-112">*Font*</span></span> | <span data-ttu-id="9d659-113">對應至字型名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="9d659-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d659-114">備註</span><span class="sxs-lookup"><span data-stu-id="9d659-114">Remarks</span></span>

<span data-ttu-id="9d659-115">**FontName** 屬性會定義在字元的快顯功能表中用來顯示文字的字型。</span><span class="sxs-lookup"><span data-stu-id="9d659-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="9d659-116">字型設定的預設值是以字元的 **LanguageID** 設定的功能表字型設定為基礎，如果未設定則為---使用者預設語言識別項設定。</span><span class="sxs-lookup"><span data-stu-id="9d659-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="9d659-117">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9d659-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




