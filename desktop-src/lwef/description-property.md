---
title: '描述屬性 (舊版 Windows 環境功能) '
description: Description 屬性
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024428"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="1f502-103">描述屬性 (舊版 Windows 環境功能) </span><span class="sxs-lookup"><span data-stu-id="1f502-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="1f502-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1f502-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1f502-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="1f502-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1f502-106">傳回或設定字串，這個字串會指定指定字元的描述。</span><span class="sxs-lookup"><span data-stu-id="1f502-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="1f502-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="1f502-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1f502-108">*代理程式*。**( "**_CharacterID_*_" ) 的字元。描述_* \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="1f502-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="1f502-109">部分</span><span class="sxs-lookup"><span data-stu-id="1f502-109">Part</span></span>     | <span data-ttu-id="1f502-110">描述</span><span class="sxs-lookup"><span data-stu-id="1f502-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f502-111">*string*</span><span class="sxs-lookup"><span data-stu-id="1f502-111">*string*</span></span> | <span data-ttu-id="1f502-112">字串值，對應到目前語言設定)  (字元的描述。</span><span class="sxs-lookup"><span data-stu-id="1f502-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f502-113">備註</span><span class="sxs-lookup"><span data-stu-id="1f502-113">Remarks</span></span>

<span data-ttu-id="1f502-114">字元的 **描述** 可能取決於字元的 **LanguageID** 設定。</span><span class="sxs-lookup"><span data-stu-id="1f502-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="1f502-115">一種語言的字元名稱可能不同，或使用不同于另一個語言的字元。</span><span class="sxs-lookup"><span data-stu-id="1f502-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="1f502-116">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義特定語言的字元預設 **描述** 。</span><span class="sxs-lookup"><span data-stu-id="1f502-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="1f502-117">[ **描述** ] 屬性設定為選擇性，而且可能不會提供給所有字元。</span><span class="sxs-lookup"><span data-stu-id="1f502-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




