---
description: Language 資料類型是包含一或多個有效數字語言識別項的文字字串。 如果有兩個以上的語言識別項，則必須以逗號分隔。
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: 語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191374"
---
# <a name="language"></a><span data-ttu-id="fc3da-104">語言</span><span class="sxs-lookup"><span data-stu-id="fc3da-104">Language</span></span>

<span data-ttu-id="fc3da-105">Language 資料類型是包含一或多個有效數字語言識別項的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fc3da-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="fc3da-106">如果有兩個以上的語言識別項，則必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="fc3da-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="fc3da-107">Language 資料類型是16位的值，也就是主要和子語言數值識別碼的組合。</span><span class="sxs-lookup"><span data-stu-id="fc3da-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="fc3da-108">主要 LANGID 由位0到9組成，而子語言識別項是位10到15。</span><span class="sxs-lookup"><span data-stu-id="fc3da-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="fc3da-109">如需主要和次要語言數值識別碼的清單，請參閱 [語言識別項常數和字串](../intl/language-identifier-constants-and-strings.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="fc3da-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="fc3da-110">針對主要語言識別項，0x200 至0x3ff 的範圍是由使用者定義的。</span><span class="sxs-lookup"><span data-stu-id="fc3da-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="fc3da-111">0x000 至0x1ff 的範圍保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="fc3da-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="fc3da-112">若為子語言識別項，則會以使用者可定義的範圍0x20 至0x3f。</span><span class="sxs-lookup"><span data-stu-id="fc3da-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="fc3da-113">從0x00 到0x1f 的範圍是保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="fc3da-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
