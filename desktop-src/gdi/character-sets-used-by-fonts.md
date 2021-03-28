---
description: 所有字型都使用字元集。 字元集包含標點符號、數位、大寫和小寫字母，以及所有其他可列印字元。 字元集的每個專案都是以數位來識別。
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: 字型所使用的字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972772"
---
# <a name="character-sets-used-by-fonts"></a><span data-ttu-id="26e76-105">字型所使用的字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-105">Character Sets Used by Fonts</span></span>

<span data-ttu-id="26e76-106">所有字型都使用字元集。</span><span class="sxs-lookup"><span data-stu-id="26e76-106">All fonts use a character set.</span></span> <span data-ttu-id="26e76-107">字元集包含標點符號、數位、大寫和小寫字母，以及所有其他可列印字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-107">A character set contains punctuation marks, numerals, uppercase and lowercase letters, and all other printable characters.</span></span> <span data-ttu-id="26e76-108">字元集的每個專案都是以數位來識別。</span><span class="sxs-lookup"><span data-stu-id="26e76-108">Each element of a character set is identified by a number.</span></span>

<span data-ttu-id="26e76-109">大部分使用中的字元集都是美國 ASCII 字元集的超集合，它會定義32到127的96數值字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-109">Most character sets in use are supersets of the U.S. ASCII character set, which defines characters for the 96 numeric values from 32 through 127.</span></span> <span data-ttu-id="26e76-110">字元集有五個主要群組：</span><span class="sxs-lookup"><span data-stu-id="26e76-110">There are five major groups of character sets:</span></span>

-   <span data-ttu-id="26e76-111">Windows</span><span class="sxs-lookup"><span data-stu-id="26e76-111">Windows</span></span>
-   <span data-ttu-id="26e76-112">Unicode</span><span class="sxs-lookup"><span data-stu-id="26e76-112">Unicode</span></span>
-   <span data-ttu-id="26e76-113">OEM (原始設備製造商)</span><span class="sxs-lookup"><span data-stu-id="26e76-113">OEM (original equipment manufacturer)</span></span>
-   <span data-ttu-id="26e76-114">符號</span><span class="sxs-lookup"><span data-stu-id="26e76-114">Symbol</span></span>
-   <span data-ttu-id="26e76-115">特定廠商</span><span class="sxs-lookup"><span data-stu-id="26e76-115">Vendor-specific</span></span>

## <a name="windows-character-set"></a><span data-ttu-id="26e76-116">Windows 字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-116">Windows Character Set</span></span>

<span data-ttu-id="26e76-117">Windows 字元集是最常使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="26e76-117">The Windows character set is the most commonly used character set.</span></span> <span data-ttu-id="26e76-118">它基本上相當於 ANSI 字元集。</span><span class="sxs-lookup"><span data-stu-id="26e76-118">It is essentially equivalent to the ANSI character set.</span></span> <span data-ttu-id="26e76-119">空白字元是 Windows 字元集中的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-119">The blank character is the first character in the Windows character set.</span></span> <span data-ttu-id="26e76-120">它的十六進位值為 0x20 (decimal 32) 。</span><span class="sxs-lookup"><span data-stu-id="26e76-120">It has a hexadecimal value of 0x20 (decimal 32).</span></span> <span data-ttu-id="26e76-121">Windows 字元集中的最後一個字元具有十六進位值 0xFF (decimal 255) 。</span><span class="sxs-lookup"><span data-stu-id="26e76-121">The last character in the Windows character set has a hexadecimal value of 0xFF (decimal 255).</span></span>

<span data-ttu-id="26e76-122">許多字型會指定預設字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-122">Many fonts specify a default character.</span></span> <span data-ttu-id="26e76-123">只要針對不在字型中的字元提出要求，系統就會提供此預設字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-123">Whenever a request is made for a character that is not in the font, the system provides this default character.</span></span> <span data-ttu-id="26e76-124">使用 Windows 字元集的許多字型都會指定句點 (。 ) 為預設字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-124">Many fonts using the Windows character set specify the period (.) as the default character.</span></span> <span data-ttu-id="26e76-125">TrueType 和 OpenType 字型通常會使用開放方塊作為預設字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-125">TrueType and OpenType fonts typically use an open box as the default character.</span></span>

<span data-ttu-id="26e76-126">字型使用稱為四的分隔字元來分隔單字和對齊文字。</span><span class="sxs-lookup"><span data-stu-id="26e76-126">Fonts use a break character called a quad to separate words and justify text.</span></span> <span data-ttu-id="26e76-127">大部分使用 Windows 字元集的字型都會指定空白字元將作為 break 字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-127">Most fonts using the Windows character set specify that the blank character will serve as the break character.</span></span>

## <a name="unicode-character-set"></a><span data-ttu-id="26e76-128">Unicode 字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-128">Unicode Character Set</span></span>

<span data-ttu-id="26e76-129">Windows 字元集會使用8個位來代表每個字元;因此，可以使用8位表示的最大字元數為 256 (2 ^ 8) 。</span><span class="sxs-lookup"><span data-stu-id="26e76-129">The Windows character set uses 8 bits to represent each character; therefore, the maximum number of characters that can be expressed using 8 bits is 256 (2^8).</span></span> <span data-ttu-id="26e76-130">這通常就足以滿足西方語言的需求，包括法文、德文、西班牙文和其他語言所使用的變音符號。</span><span class="sxs-lookup"><span data-stu-id="26e76-130">This is usually sufficient for Western languages, including the diacritical marks used in French, German, Spanish, and other languages.</span></span> <span data-ttu-id="26e76-131">不過，東部語言採用數以千計的不同字元，無法使用單一位元組編碼配置進行編碼。</span><span class="sxs-lookup"><span data-stu-id="26e76-131">However, Eastern languages employ thousands of separate characters, which cannot be encoded by using a single-byte coding scheme.</span></span> <span data-ttu-id="26e76-132">隨著電腦 commerce 的激增，已開發雙位元組編碼配置，因此可以在8位、16位、24位或32位序列中表示字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-132">With the proliferation of computer commerce, double-byte coding schemes were developed so that characters could be represented in 8-bit, 16-bit, 24-bit, or 32-bit sequences.</span></span> <span data-ttu-id="26e76-133">這需要複雜的傳遞演算法;如此一來，使用不同的程式碼集會在兩部不同的電腦上產生完全不同的結果。</span><span class="sxs-lookup"><span data-stu-id="26e76-133">This requires complicated passing algorithms; even so, using different code sets could yield entirely different results on two different computers.</span></span>

<span data-ttu-id="26e76-134">為了解決多個程式碼撰寫架構的問題，已開發出資料標記法的 Unicode 標準。</span><span class="sxs-lookup"><span data-stu-id="26e76-134">To address the problem of multiple coding schemes, the Unicode standard for data representation was developed.</span></span> <span data-ttu-id="26e76-135">16位字元編碼配置，Unicode 可以代表 65536 (2 ^ 16) 個字元，這足以包含目前電腦 commerce 中的所有語言，以及標點符號、數學符號和擴充的空間。</span><span class="sxs-lookup"><span data-stu-id="26e76-135">A 16-bit character coding scheme, Unicode can represent 65,536 (2^16) characters, which is enough to include all languages in computer commerce today, as well as punctuation marks, mathematical symbols, and room for expansion.</span></span> <span data-ttu-id="26e76-136">Unicode 會為每個字元建立唯一的程式碼，以確保字元轉譯永遠正確。</span><span class="sxs-lookup"><span data-stu-id="26e76-136">Unicode establishes a unique code for every character to ensure that character translation is always accurate.</span></span>

## <a name="oem-character-set"></a><span data-ttu-id="26e76-137">OEM 字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-137">OEM Character Set</span></span>

<span data-ttu-id="26e76-138">OEM 字元集通常用於螢幕顯示的全螢幕 MS-DOS 會話中。</span><span class="sxs-lookup"><span data-stu-id="26e76-138">The OEM character set is typically used in full-screen MS-DOS sessions for screen display.</span></span> <span data-ttu-id="26e76-139">在 OEM、美國 ASCII 和 Windows 字元集中，字元32到127通常相同。</span><span class="sxs-lookup"><span data-stu-id="26e76-139">Characters 32 through 127 are usually the same in the OEM, U.S. ASCII, and Windows character sets.</span></span> <span data-ttu-id="26e76-140">OEM 字元集中的其他字元 (0 到31和128到 255) 對應到可在全螢幕 MS-DOS 會話中顯示的字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-140">The other characters in the OEM character set (0 through 31 and 128 through 255) correspond to the characters that can be displayed in a full-screen MS-DOS session.</span></span> <span data-ttu-id="26e76-141">這些字元通常與 Windows 字元不同。</span><span class="sxs-lookup"><span data-stu-id="26e76-141">These characters are generally different from the Windows characters.</span></span>

## <a name="symbol-character-set"></a><span data-ttu-id="26e76-142">符號字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-142">Symbol Character Set</span></span>

<span data-ttu-id="26e76-143">符號字元集包含通常用來表示數學和科學公式的特殊字元。</span><span class="sxs-lookup"><span data-stu-id="26e76-143">The Symbol character set contains special characters typically used to represent mathematical and scientific formulas.</span></span>

## <a name="vendor-specific-character-sets"></a><span data-ttu-id="26e76-144">廠商特定字元集</span><span class="sxs-lookup"><span data-stu-id="26e76-144">Vendor-Specific Character Sets</span></span>

<span data-ttu-id="26e76-145">許多印表機和其他輸出裝置會根據與 Windows 和 OEM setsfor 範例不同的字元集提供字型， (EBCDIC) 字元集的擴充二進位編碼十進位交換程式碼。</span><span class="sxs-lookup"><span data-stu-id="26e76-145">Many printers and other output devices provide fonts based on character sets that differ from the Windows and OEM setsfor example, the Extended Binary Coded Decimal Interchange Code (EBCDIC) character set.</span></span> <span data-ttu-id="26e76-146">若要使用這些字元集的其中一個，印表機驅動程式會從 Windows 字元集轉譯為廠商特定字元集。</span><span class="sxs-lookup"><span data-stu-id="26e76-146">To use one of these character sets, the printer driver translates from the Windows character set to the vendor-specific character set.</span></span>

 

 



