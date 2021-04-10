---
title: 'Caption 屬性 (命令集合物件) '
description: Caption 屬性
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093639"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="70e7d-103">Caption 屬性 (命令集合物件) </span><span class="sxs-lookup"><span data-stu-id="70e7d-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="70e7d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="70e7d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="70e7d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="70e7d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="70e7d-106">決定在字元的快顯功能表中針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="70e7d-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="70e7d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="70e7d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="70e7d-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。_ \*[命令。標題](caption-property.md) \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="70e7d-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="70e7d-109">部分</span><span class="sxs-lookup"><span data-stu-id="70e7d-109">Part</span></span>     | <span data-ttu-id="70e7d-110">描述</span><span class="sxs-lookup"><span data-stu-id="70e7d-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="70e7d-111">*string*</span><span class="sxs-lookup"><span data-stu-id="70e7d-111">*string*</span></span> | <span data-ttu-id="70e7d-112">評估為顯示為標題之文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="70e7d-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70e7d-113">備註</span><span class="sxs-lookup"><span data-stu-id="70e7d-113">Remarks</span></span>

<span data-ttu-id="70e7d-114">設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性，可定義當其 [**Visible**](visible-property.md)屬性設定為 True 且您的應用程式不是輸入-主動用戶端時，它會在字元的快顯功能表上顯示的方式。</span><span class="sxs-lookup"><span data-stu-id="70e7d-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="70e7d-115">若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。</span><span class="sxs-lookup"><span data-stu-id="70e7d-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="70e7d-116">如果您針對具有 [**標題**](caption-property.md)的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合定義命令，您通常也會為其相關聯的 **命令** 集合定義 **標題**。</span><span class="sxs-lookup"><span data-stu-id="70e7d-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
