---
description: 使用者自訂字元 (在雙位元組字元集中的 EUDC)  (Dbcs) 和私用區域 (PUA) Unicode 字元是自訂字元。
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: 終端使用者定義和私用區域字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320232"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="b3a39-103">終端使用者定義和私用區域字元</span><span class="sxs-lookup"><span data-stu-id="b3a39-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="b3a39-104">使用者自訂字元 (在 [雙位元組字元集](double-byte-character-sets.md) 中的 EUDC)  (dbcs) 和私用區域 (PUA) [Unicode](unicode.md) 字元是自訂字元。</span><span class="sxs-lookup"><span data-stu-id="b3a39-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="b3a39-105">您可以由使用者或其他合作物件（例如設備製造商、使用者群組、政府機構或字型設計公司）來定義和執行這些用戶端。</span><span class="sxs-lookup"><span data-stu-id="b3a39-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="b3a39-106">其用途可讓使用者使用標準螢幕和印表機字型中未提供的字元來形成名稱和其他文字。</span><span class="sxs-lookup"><span data-stu-id="b3a39-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="b3a39-107">您可以在不同的電腦上，以不同的方式指派 EUDC 和 PUA 字元。</span><span class="sxs-lookup"><span data-stu-id="b3a39-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="b3a39-108">某些字碼頁有可重複使用 EUDC 範圍的延伸模組，而這些延伸模組可能會彼此衝突。</span><span class="sxs-lookup"><span data-stu-id="b3a39-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="b3a39-109">在其他情況下，製造商可能會在其中一個範圍內提供一組自訂字元。</span><span class="sxs-lookup"><span data-stu-id="b3a39-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="b3a39-110">此外，使用者群組也可以嘗試在 PUA 中提供額外的字元。</span><span class="sxs-lookup"><span data-stu-id="b3a39-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="b3a39-111">這些案例的不同組合可能會造成衝突。</span><span class="sxs-lookup"><span data-stu-id="b3a39-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="b3a39-112">建立依賴 EUDC 或 PUA 字元的應用程式時，您應該記住個別程式碼點的衝突解釋。</span><span class="sxs-lookup"><span data-stu-id="b3a39-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="b3a39-113">下列主題討論支援 EUDCs 的字型，以及這些字元的存取和管理：</span><span class="sxs-lookup"><span data-stu-id="b3a39-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="b3a39-114">字元集和字型</span><span class="sxs-lookup"><span data-stu-id="b3a39-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="b3a39-115">EUDC 登錄專案</span><span class="sxs-lookup"><span data-stu-id="b3a39-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="b3a39-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3a39-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3a39-117">關於 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="b3a39-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



