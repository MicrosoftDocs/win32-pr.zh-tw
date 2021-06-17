---
title: 'Caption 屬性 (Command 物件) '
description: 瞭解 Command 物件的 Caption 屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262550"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="e7180-104">Caption 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="e7180-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="e7180-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e7180-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e7180-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="e7180-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e7180-107">決定在指定的字元快顯功能表中針對 [**命令**](/windows/desktop/lwef/the-command-object) 顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="e7180-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="e7180-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="e7180-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e7180-109">\*代理程式 \***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_\*_"。標題_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="e7180-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="e7180-110">部分</span><span class="sxs-lookup"><span data-stu-id="e7180-110">Part</span></span>     | <span data-ttu-id="e7180-111">描述</span><span class="sxs-lookup"><span data-stu-id="e7180-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7180-112">*string*</span><span class="sxs-lookup"><span data-stu-id="e7180-112">*string*</span></span> | <span data-ttu-id="e7180-113">評估為顯示為 **命令** 標題之文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="e7180-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7180-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7180-114">Remarks</span></span>

<span data-ttu-id="e7180-115">若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。</span><span class="sxs-lookup"><span data-stu-id="e7180-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="e7180-116">如果您未定義命令的 **VoiceCaption** ，則會使用您的 **標題** 設定。</span><span class="sxs-lookup"><span data-stu-id="e7180-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
