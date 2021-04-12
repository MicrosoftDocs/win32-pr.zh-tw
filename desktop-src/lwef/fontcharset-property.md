---
title: FontCharSet 屬性
description: FontCharSet 屬性
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301855"
---
# <a name="fontcharset-property"></a><span data-ttu-id="50605-103">FontCharSet 屬性</span><span class="sxs-lookup"><span data-stu-id="50605-103">FontCharSet Property</span></span>

<span data-ttu-id="50605-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="50605-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="50605-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="50605-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="50605-106">傳回或設定在指定字元的字提示字元中顯示之字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="50605-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="50605-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="50605-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="50605-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。FontCharSet* \*  \[  =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="50605-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="50605-109">部分</span><span class="sxs-lookup"><span data-stu-id="50605-109">Part</span></span>    | <span data-ttu-id="50605-110">描述</span><span class="sxs-lookup"><span data-stu-id="50605-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50605-111">*value*</span><span class="sxs-lookup"><span data-stu-id="50605-111">*value*</span></span> | <span data-ttu-id="50605-112">整數值，指定字型所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="50605-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="50605-113">以下是值：0標準 Windows 字元 (ANSI) 的一些常見設定。</span><span class="sxs-lookup"><span data-stu-id="50605-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="50605-114">1個預設字元集。</span><span class="sxs-lookup"><span data-stu-id="50605-114">1 Default character set.</span></span><br/> <span data-ttu-id="50605-115">2符號字元集。</span><span class="sxs-lookup"><span data-stu-id="50605-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="50605-116">128在日文版的 Windows 中， (DBCS) 獨特的雙位元組字元集。</span><span class="sxs-lookup"><span data-stu-id="50605-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="50605-117">129的雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。</span><span class="sxs-lookup"><span data-stu-id="50605-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="50605-118">134的雙位元組字元集 (DBCS) Windows 的簡體中文版本獨有。</span><span class="sxs-lookup"><span data-stu-id="50605-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="50605-119">136的雙位元組字元集 (DBCS) 對繁體中文 Windows 而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="50605-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="50605-120">255通常由 Microsoft MS-DOS 應用程式所顯示的擴充字元。</span><span class="sxs-lookup"><span data-stu-id="50605-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="50605-121">如需其他字元集值，請參閱 Platform SDK 檔集。</span><span class="sxs-lookup"><span data-stu-id="50605-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50605-122">備註</span><span class="sxs-lookup"><span data-stu-id="50605-122">Remarks</span></span>

<span data-ttu-id="50605-123">在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字元集的預設值。</span><span class="sxs-lookup"><span data-stu-id="50605-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="50605-124">此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字元集設定。</span><span class="sxs-lookup"><span data-stu-id="50605-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="50605-125">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="50605-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="50605-126">如果您使用未編譯的字元，請檢查字元的 [**FontName**](fontname-property.md) 和 **FontCharSet** 屬性，以判斷它們是否適用于您的地區設定。</span><span class="sxs-lookup"><span data-stu-id="50605-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="50605-127">您可能必須先設定這些值，然後才能使用 [ [**朗讀**](speak-method.md) ] 方法，以確保文字顯示在 [文字] 氣球內的適當文字。</span><span class="sxs-lookup"><span data-stu-id="50605-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="50605-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50605-128">See Also</span></span>

[<span data-ttu-id="50605-129">**FontName 屬性**</span><span class="sxs-lookup"><span data-stu-id="50605-129">**FontName property**</span></span>](fontname-property.md)


 

 





