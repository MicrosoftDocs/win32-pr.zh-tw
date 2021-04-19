---
description: 一律在 Unicode 純文字檔前面加上位元組順序標記，這會通知應用程式接收檔案的位元組順序。
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: 使用位元組順序標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000199"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="4a6e9-103">使用位元組順序標記</span><span class="sxs-lookup"><span data-stu-id="4a6e9-103">Using Byte Order Marks</span></span>

<span data-ttu-id="4a6e9-104">一律在 Unicode 純文字檔前面加上位元組順序標記，這會通知應用程式接收檔案的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="4a6e9-105">下表列出可用的位元組順序標記。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="4a6e9-106">因為 Unicode 純文字是16位程式碼值的序列，所以它會區分寫入文字時使用的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="4a6e9-107">位元組順序標記不是選取文字位元組順序的控制字元。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="4a6e9-108">位元組順序符號</span><span class="sxs-lookup"><span data-stu-id="4a6e9-108">Byte order mark</span></span> | <span data-ttu-id="4a6e9-109">Description</span><span class="sxs-lookup"><span data-stu-id="4a6e9-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="4a6e9-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="4a6e9-110">EF BB BF</span></span>        | <span data-ttu-id="4a6e9-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="4a6e9-111">UTF-8</span></span>                 |
| <span data-ttu-id="4a6e9-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="4a6e9-112">FF FE</span></span>           | <span data-ttu-id="4a6e9-113">UTF-16、位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="4a6e9-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="4a6e9-114">FE FF</span><span class="sxs-lookup"><span data-stu-id="4a6e9-114">FE FF</span></span>           | <span data-ttu-id="4a6e9-115">UTF-16、big endian</span><span class="sxs-lookup"><span data-stu-id="4a6e9-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="4a6e9-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="4a6e9-116">FF FE 00 00</span></span>     | <span data-ttu-id="4a6e9-117">UTF-32，位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="4a6e9-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="4a6e9-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="4a6e9-118">00 00 FE FF</span></span>     | <span data-ttu-id="4a6e9-119">32 UTF-8、位元組由大到小</span><span class="sxs-lookup"><span data-stu-id="4a6e9-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="4a6e9-120">Microsoft 使用 UTF-16、位元組由小到小的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="4a6e9-121">在理想的情況下，所有 Unicode 文字只會遵循一組位元組順序規則。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="4a6e9-122">不過，這並不可行，因為微處理器在放置最不重要的位元組時，會有所不同。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="4a6e9-123">Intel 和 MIPS 處理器會先定位最不重要的位元組，而 Motorola 處理器 (和所有位元組反向的 Unicode 檔案) 定位到最後一個位置。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="4a6e9-124">只有一組位元組順序規則，每次讀取或寫入純文字檔時，一種類型的微處理器的使用者都會強制交換位元組順序，即使檔案永遠不會根據不同的微處理器傳送到另一個作業系統。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="4a6e9-125">指定位元組順序的慣用位置是在檔案標頭中，但是文字檔沒有標頭。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="4a6e9-126">因此，Unicode 已定義字元 (U + FEFF) ，而非字元 (U + FFFE) 為位元組順序標記。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="4a6e9-127">它們是彼此的鏡像位元組影像。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="4a6e9-128">由於序列 U + FEFF 在一般非 Unicode 文字檔的開頭非常罕見，因此可以作為隱含標記或簽章，以將檔案識別為 Unicode 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="4a6e9-129">同時讀取 Unicode 和非 Unicode 文字檔的應用程式應該使用此順序的存在，作為檔案最可能是 Unicode 檔案的指標。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="4a6e9-130">比較這項技術與使用 MS-DOS EOF 標記來終止文字檔。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="4a6e9-131">當應用程式在文字檔的開頭找到 U + FEFF 時，它通常會將檔案處理為 Unicode 檔案，但它可以執行進一步的啟發式檢查以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="4a6e9-132">這樣的檢查可以像測試一樣簡單，找出低序位位元組的變化是否遠高於高序位位元組的變化。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="4a6e9-133">例如，如果 ASCII 文字轉換成 Unicode 文字，則每秒的位元組都是0。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="4a6e9-134">此外，同時檢查換行字元和換行字元 (U + 000A 和 U + 000D) ，甚至或奇數檔案大小，都可以提供檔案本質的強式指標。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="4a6e9-135">當應用程式在文字檔的開頭找到 U + FFFE 時，它會將它解讀為表示檔案是位元組反轉的 Unicode 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="4a6e9-136">應用程式可以交換位元組的順序，或警示使用者發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="4a6e9-137">因為在任何字碼頁中找不到 Unicode 位元組順序標記字元，所以如果資料轉換成 ANSI，它就會消失。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="4a6e9-138">不同于其他 Unicode 字元，轉換時不會以預設字元取代。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="4a6e9-139">如果在檔案中間找到位元組順序標記，則不會將它視為 Unicode 字元，而且對文字輸出沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="4a6e9-140">Unicode 值 U + FFFF 在純文字檔中是不合法的，而且無法在應用程式之間傳遞。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="4a6e9-141">它是保留供私用應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4a6e9-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4a6e9-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a6e9-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a6e9-143">使用 Unicode 中的特殊字元</span><span class="sxs-lookup"><span data-stu-id="4a6e9-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



