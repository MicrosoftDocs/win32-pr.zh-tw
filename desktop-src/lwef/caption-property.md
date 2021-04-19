---
title: 'Caption 屬性 (Command 物件) '
description: Caption 屬性
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968130"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="9d7db-103">Caption 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="9d7db-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="9d7db-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9d7db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9d7db-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="9d7db-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9d7db-106">決定在指定的字元快顯功能表中針對 [**命令**](/windows/desktop/lwef/the-command-object) 顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="9d7db-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="9d7db-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="9d7db-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9d7db-108">\*代理程式 \***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_\*_"。標題_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="9d7db-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="9d7db-109">部分</span><span class="sxs-lookup"><span data-stu-id="9d7db-109">Part</span></span>     | <span data-ttu-id="9d7db-110">描述</span><span class="sxs-lookup"><span data-stu-id="9d7db-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7db-111">*string*</span><span class="sxs-lookup"><span data-stu-id="9d7db-111">*string*</span></span> | <span data-ttu-id="9d7db-112">評估為顯示為 **命令** 標題之文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="9d7db-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d7db-113">備註</span><span class="sxs-lookup"><span data-stu-id="9d7db-113">Remarks</span></span>

<span data-ttu-id="9d7db-114">若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。</span><span class="sxs-lookup"><span data-stu-id="9d7db-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="9d7db-115">如果您未定義命令的 **VoiceCaption** ，則會使用您的 **標題** 設定。</span><span class="sxs-lookup"><span data-stu-id="9d7db-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
