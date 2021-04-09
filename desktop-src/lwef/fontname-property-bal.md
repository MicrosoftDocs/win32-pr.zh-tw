---
title: 'FontName 屬性 (Balloon 物件) '
description: FontName 屬性
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093684"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="807c7-103">FontName 屬性 (Balloon 物件) </span><span class="sxs-lookup"><span data-stu-id="807c7-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="807c7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="807c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="807c7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="807c7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="807c7-106">傳回或設定指定字元之文字批註中所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="807c7-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="807c7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="807c7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="807c7-108">\*agent. \***字元 ( "**_CharacterID_\*_" ) 。FontName_ \*  \[  =  *字型*\]</span><span class="sxs-lookup"><span data-stu-id="807c7-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="807c7-109">部分</span><span class="sxs-lookup"><span data-stu-id="807c7-109">Part</span></span>   | <span data-ttu-id="807c7-110">描述</span><span class="sxs-lookup"><span data-stu-id="807c7-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="807c7-111">*字體*</span><span class="sxs-lookup"><span data-stu-id="807c7-111">*font*</span></span> | <span data-ttu-id="807c7-112">對應至字型名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="807c7-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="807c7-113">備註</span><span class="sxs-lookup"><span data-stu-id="807c7-113">Remarks</span></span>

<span data-ttu-id="807c7-114">[**FontName**](fontname-property.md)屬性會定義用來在字串的文字氣球視窗中顯示文字的字型。</span><span class="sxs-lookup"><span data-stu-id="807c7-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="807c7-115">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="807c7-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="807c7-116">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。</span><span class="sxs-lookup"><span data-stu-id="807c7-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="807c7-117">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="807c7-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="807c7-118">如果您使用未編譯的字元，請檢查字元的 [**FontName**](fontname-property.md) 和 [**FontCharSet**](fontcharset-property.md) 屬性，以判斷它們是否適用于您的地區設定。</span><span class="sxs-lookup"><span data-stu-id="807c7-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="807c7-119">您可能必須先設定這些值，然後才能使用 [ [**朗讀**](speak-method.md) ] 方法，以確保文字顯示在 [文字] 氣球內的適當文字。</span><span class="sxs-lookup"><span data-stu-id="807c7-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




