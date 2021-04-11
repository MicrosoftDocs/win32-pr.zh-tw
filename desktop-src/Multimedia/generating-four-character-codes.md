---
title: 產生 Four-Character 碼
description: 產生 Four-Character 碼
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- 多媒體檔案 i/o，四個字元的代碼
- 檔案 i/o，四個字元的代碼
- 輸入和輸出 (i/o) ，四個字元的代碼
- I/o (輸入和輸出) 四個字元的代碼
- 四個字元的代碼
- mmioStringToFOURCC 函式
- mmioFOURCC 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681813"
---
# <a name="generating-four-character-codes"></a><span data-ttu-id="c078b-110">產生 Four-Character 碼</span><span class="sxs-lookup"><span data-stu-id="c078b-110">Generating Four-Character Codes</span></span>

<span data-ttu-id="c078b-111">您可以使用 [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) 宏或 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) 函數來產生四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="c078b-111">You can use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro or the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function to generate four-character codes.</span></span> <span data-ttu-id="c078b-112">下列範例會使用 **mmioFOURCC** ，為 "WAVE" 產生四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="c078b-112">The following example uses **mmioFOURCC** to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



<span data-ttu-id="c078b-113">下列範例會使用 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) ，為 "WAVE" 產生四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="c078b-113">The following example uses [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



<span data-ttu-id="c078b-114">[**MmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)中的第二個參數會指定用來將字串轉換成四個字元代碼的旗標。</span><span class="sxs-lookup"><span data-stu-id="c078b-114">The second parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifies flags for converting the string to a four-character code.</span></span> <span data-ttu-id="c078b-115">如果您指定 MMIO \_ TOUPPER 旗標， **mmioStringToFOURCC** 會將字串中的所有字母字元轉換成大寫。</span><span class="sxs-lookup"><span data-stu-id="c078b-115">If you specify the MMIO\_TOUPPER flag, **mmioStringToFOURCC** converts all alphabetic characters in the string to uppercase.</span></span> <span data-ttu-id="c078b-116">當您需要指定四個字元的代碼來識別自訂 i/o 程式時，這會很有用，因為識別副檔名的四個字元的程式碼必須全部都是大寫。</span><span class="sxs-lookup"><span data-stu-id="c078b-116">This is useful when you need to specify a four-character code to identify a custom I/O procedure because four-character codes identifying file-extension names must be all uppercase.</span></span>

 

 