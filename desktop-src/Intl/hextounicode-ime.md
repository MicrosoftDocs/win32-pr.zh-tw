---
description: Rich Edit 3.0 支援 HexToUnicode IME，可讓使用者以兩種方式的其中一種，使用快速鍵在十六進位和 Unicode 字元之間進行轉換。
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514204"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="0b94d-103">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="0b94d-103">HexToUnicode IME</span></span>

<span data-ttu-id="0b94d-104">Rich Edit 3.0 支援 HexToUnicode IME，可讓使用者以兩種方式的其中一種，使用快速鍵在十六進位和 Unicode 字元之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="0b94d-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="0b94d-105">使用第一個轉換方法，使用者以十六進位鍵入字元碼，然後輸入 ALT + X。</span><span class="sxs-lookup"><span data-stu-id="0b94d-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="0b94d-106">IME 會以 Unicode 字元取代插入點前面的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="0b94d-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="0b94d-107">如果目前的字型不支援字元碼，則會選擇支援它的適當字型。</span><span class="sxs-lookup"><span data-stu-id="0b94d-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="0b94d-108">若要從 Unicode 轉換為十六進位，使用者可輸入 SHIFT + ALT + X。</span><span class="sxs-lookup"><span data-stu-id="0b94d-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="0b94d-109">這個專案會將插入點前面的 Unicode 字元取代為十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="0b94d-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="0b94d-110">尤其是，此方法可讓使用者判斷「遺漏圖像」指標所表示的字元。</span><span class="sxs-lookup"><span data-stu-id="0b94d-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="0b94d-111">如果十六進位字元碼緊接在某些合法的 (非字元) 十六進位字元，使用者會選取要在輸入 ALT + X 之前轉換的特定數位。</span><span class="sxs-lookup"><span data-stu-id="0b94d-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="0b94d-112">第一個方法的問題是，ALT + X 有時會用來做為 exit 命令的按鍵組合 (也就是 eXit) 。</span><span class="sxs-lookup"><span data-stu-id="0b94d-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="0b94d-113">例如，在 Microsoft Office 中，此命令只會 **顯示為 [檔案] 功能表的** 選項。</span><span class="sxs-lookup"><span data-stu-id="0b94d-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="0b94d-114">在十六進位和 Unicode 字元之間轉換的第二種方法牽涉到數位板。</span><span class="sxs-lookup"><span data-stu-id="0b94d-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="0b94d-115">使用這個方法時，使用者可以輸入 ALT + NumPad 數位 (值大於 255) ，以使用十進位值輸入 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="0b94d-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="0b94d-116">這個方法與第一個方法並不一樣，因為使用者無法看到輸入了哪些十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="0b94d-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="0b94d-117">此外，使用者不能更正十六進位數位，除非重新輸入所有數位。</span><span class="sxs-lookup"><span data-stu-id="0b94d-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b94d-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b94d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b94d-119">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="0b94d-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



