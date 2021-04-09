---
title: 'VoiceCaption 屬性 (命令物件) '
description: VoiceCaption 屬性
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685402"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="8b700-103">VoiceCaption 屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="8b700-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="8b700-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8b700-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8b700-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="8b700-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8b700-106">傳回或設定 [語音命令] 視窗中針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="8b700-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="8b700-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="8b700-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8b700-108">\*agent. \***字元 ( "**_CharacterID_\*_" ) . VoiceCaption_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="8b700-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8b700-109">部分</span><span class="sxs-lookup"><span data-stu-id="8b700-109">Part</span></span>     | <span data-ttu-id="8b700-110">描述</span><span class="sxs-lookup"><span data-stu-id="8b700-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="8b700-111">*string*</span><span class="sxs-lookup"><span data-stu-id="8b700-111">*string*</span></span> | <span data-ttu-id="8b700-112">評估為顯示之文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="8b700-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b700-113">備註</span><span class="sxs-lookup"><span data-stu-id="8b700-113">Remarks</span></span>

<span data-ttu-id="8b700-114">如果您設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性，您通常也會設定其 **VoiceCaption** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8b700-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="8b700-115">當您的用戶端應用程式為輸入-使用中且字元可見時，[ **VoiceCaption** 文字] 設定就會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="8b700-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="8b700-116">如果未設定這個屬性， **命令** 集合的 [**Caption**](caption-property.md) 屬性的設定會決定顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="8b700-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="8b700-117">未設定 **VoiceCaption** 或 **Caption** 屬性時，當用戶端應用程式變成輸入主動時，集合中的命令會出現在 [ (未定義的命令) ] 下的 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="8b700-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="8b700-118">**VoiceCaption** 設定也會決定要在接聽提示中顯示的文字，以指出該字元接聽的命令。</span><span class="sxs-lookup"><span data-stu-id="8b700-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b700-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b700-119">See Also</span></span>

[<span data-ttu-id="8b700-120">Caption 屬性</span><span class="sxs-lookup"><span data-stu-id="8b700-120">Caption property</span></span>](caption-property.md)


 

 
