---
title: 'Name 屬性 (字元物件) '
description: Name 屬性
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464056"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="d7ec1-103">Name 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="d7ec1-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="d7ec1-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d7ec1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d7ec1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="d7ec1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d7ec1-106">傳回或設定字串，這個字串會指定指定字元的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d7ec1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="d7ec1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d7ec1-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。名稱_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="d7ec1-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="d7ec1-109">部分</span><span class="sxs-lookup"><span data-stu-id="d7ec1-109">Part</span></span>     | <span data-ttu-id="d7ec1-110">描述</span><span class="sxs-lookup"><span data-stu-id="d7ec1-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ec1-111">*string*</span><span class="sxs-lookup"><span data-stu-id="d7ec1-111">*string*</span></span> | <span data-ttu-id="d7ec1-112">字串值，對應到目前語言設定)  (的字元名稱。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7ec1-113">備註</span><span class="sxs-lookup"><span data-stu-id="d7ec1-113">Remarks</span></span>

<span data-ttu-id="d7ec1-114">字元的 **名稱** 可能取決於字元的 [**LanguageID**](languageid-property.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="d7ec1-115">一種語言的字元名稱可能不同，或使用不同于另一個語言的字元。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="d7ec1-116">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義特定語言的字元預設 **名稱** 。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d7ec1-117">避免將字元重新命名，尤其是在其他用戶端應用程式可能使用相同字元的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="d7ec1-118">此外，Agent 會使用字元的 **名稱** 自動建立隱藏和顯示字元的命令。</span><span class="sxs-lookup"><span data-stu-id="d7ec1-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




