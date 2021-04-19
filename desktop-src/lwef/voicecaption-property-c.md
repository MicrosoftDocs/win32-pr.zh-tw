---
title: 'VoiceCaption 屬性 (Command 物件) '
description: VoiceCaption 屬性
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966486"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="19d1a-103">VoiceCaption 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="19d1a-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="19d1a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="19d1a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="19d1a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="19d1a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="19d1a-106">設定或傳回 [語音命令] 視窗中針對 [**命令**](/windows/desktop/lwef/the-command-object) 物件顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="19d1a-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="19d1a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="19d1a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="19d1a-108">\*agent. \***字元 ( "**_CharacterID_*_" ) . 命令 ( "_*_Name_\*_" ) 。VoiceCaption_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="19d1a-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="19d1a-109">部分</span><span class="sxs-lookup"><span data-stu-id="19d1a-109">Part</span></span>     | <span data-ttu-id="19d1a-110">描述</span><span class="sxs-lookup"><span data-stu-id="19d1a-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="19d1a-111">*string*</span><span class="sxs-lookup"><span data-stu-id="19d1a-111">*string*</span></span> | <span data-ttu-id="19d1a-112">評估為顯示之文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="19d1a-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19d1a-113">備註</span><span class="sxs-lookup"><span data-stu-id="19d1a-113">Remarks</span></span>

<span data-ttu-id="19d1a-114">如果您在 [**命令**](https://www.bing.com/search?q=**Commands**)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="19d1a-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="19d1a-115">當您的用戶端應用程式為輸入-使用中且字元可見時，此文字會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="19d1a-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="19d1a-116">如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="19d1a-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="19d1a-117">未設定 **VoiceCaption** 或 **Caption** 屬性時，命令不會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="19d1a-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="19d1a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19d1a-118">See Also</span></span>

[<span data-ttu-id="19d1a-119">**Caption 屬性**</span><span class="sxs-lookup"><span data-stu-id="19d1a-119">**Caption property**</span></span>](caption-property.md)


 

 
