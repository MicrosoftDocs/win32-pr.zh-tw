---
title: 'Name 屬性 (字元物件) '
description: 深入瞭解字元物件的 Name 屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989323"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="044d2-104">Name 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="044d2-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="044d2-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="044d2-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="044d2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="044d2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="044d2-107">傳回或設定字串，這個字串會指定指定字元的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="044d2-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="044d2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="044d2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="044d2-109">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。名稱_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="044d2-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="044d2-110">部分</span><span class="sxs-lookup"><span data-stu-id="044d2-110">Part</span></span>     | <span data-ttu-id="044d2-111">描述</span><span class="sxs-lookup"><span data-stu-id="044d2-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="044d2-112">*string*</span><span class="sxs-lookup"><span data-stu-id="044d2-112">*string*</span></span> | <span data-ttu-id="044d2-113">字串值，對應到目前語言設定)  (的字元名稱。</span><span class="sxs-lookup"><span data-stu-id="044d2-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="044d2-114">備註</span><span class="sxs-lookup"><span data-stu-id="044d2-114">Remarks</span></span>

<span data-ttu-id="044d2-115">字元的 **名稱** 可能取決於字元的 [**LanguageID**](languageid-property.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="044d2-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="044d2-116">一種語言的字元名稱可能不同，或使用不同于另一個語言的字元。</span><span class="sxs-lookup"><span data-stu-id="044d2-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="044d2-117">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義特定語言的字元預設 **名稱** 。</span><span class="sxs-lookup"><span data-stu-id="044d2-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="044d2-118">避免將字元重新命名，尤其是在其他用戶端應用程式可能使用相同字元的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="044d2-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="044d2-119">此外，Agent 會使用字元的 **名稱** 自動建立隱藏和顯示字元的命令。</span><span class="sxs-lookup"><span data-stu-id="044d2-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




