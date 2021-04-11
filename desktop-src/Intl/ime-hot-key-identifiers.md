---
description: 這些識別碼會搭配 ImmSimulateHotKey 函式使用。
ms.assetid: a262ef4e-d8ab-4eb6-88c6-023b90850cc6
title: 輸入碼熱鍵識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407bffa76558626e88d8fbb88343d82df5557a78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113621"
---
# <a name="ime-hot-key-identifiers"></a><span data-ttu-id="38b5d-103">輸入碼熱鍵識別碼</span><span class="sxs-lookup"><span data-stu-id="38b5d-103">IME Hot Key Identifiers</span></span>

<span data-ttu-id="38b5d-104">這些識別碼會搭配 [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="38b5d-104">These identifiers are used with the [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey) function.</span></span>



| <span data-ttu-id="38b5d-105">識別碼</span><span class="sxs-lookup"><span data-stu-id="38b5d-105">Identifiers</span></span>                       | <span data-ttu-id="38b5d-106">意義</span><span class="sxs-lookup"><span data-stu-id="38b5d-106">Meaning</span></span>                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b5d-107">輸入法 \_ CHOTKEY \_ IME \_ NONIME \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-107">IME\_CHOTKEY\_IME\_NONIME\_TOGGLE</span></span> | <span data-ttu-id="38b5d-108">當語言為簡體中文時， (簡體中文) 在輸入法和非 IME 作業之間切換。</span><span class="sxs-lookup"><span data-stu-id="38b5d-108">(Simplified Chinese) Toggle between IME and non-IME operation when the language is Simplified Chinese.</span></span>                                                                                                  |
| <span data-ttu-id="38b5d-109">IME \_ CHOTKEY \_ 圖形 \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-109">IME\_CHOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="38b5d-110"> (簡體中文) 切換 IME 的圖形轉換模式。</span><span class="sxs-lookup"><span data-stu-id="38b5d-110">(Simplified Chinese) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                           |
| <span data-ttu-id="38b5d-111">IME \_ CHOTKEY \_ 符號 \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-111">IME\_CHOTKEY\_SYMBOL\_TOGGLE</span></span>      | <span data-ttu-id="38b5d-112"> (簡體中文) 切換 IME 的符號轉換模式。</span><span class="sxs-lookup"><span data-stu-id="38b5d-112">(Simplified Chinese) Toggle the symbol conversion mode of IME.</span></span> <span data-ttu-id="38b5d-113">符號模式表示使用者可以藉由對應至鍵盤上的標點符號和符號來輸入中文標點符號和符號。</span><span class="sxs-lookup"><span data-stu-id="38b5d-113">Symbol mode indicates that the user can input Chinese punctuation and symbols by mapping to the punctuation and symbols on the keyboard.</span></span> |
| <span data-ttu-id="38b5d-114">IME \_ ITHOTKEY \_ RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="38b5d-114">IME\_ITHOTKEY\_RECONVERTSTRING</span></span>    | <span data-ttu-id="38b5d-115">**Windows Me/98、windows 2000、WINDOWS XP：** (的繁體中文) 觸發程式重組。</span><span class="sxs-lookup"><span data-stu-id="38b5d-115">**Windows Me/98, Windows 2000, Windows XP:** (Traditional Chinese) Trigger reconversion.</span></span>                                                                                                                |
| <span data-ttu-id="38b5d-116">輸入法 \_ JHOTKEY \_ 關閉 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="38b5d-116">IME\_JHOTKEY\_CLOSE\_OPEN</span></span>         | <span data-ttu-id="38b5d-117"> (日文) 也開啟並關閉 IME。</span><span class="sxs-lookup"><span data-stu-id="38b5d-117">(Japanese) Alternately open and close the IME.</span></span>                                                                                                                                                          |
| <span data-ttu-id="38b5d-118">IME \_ KHOTKEY \_ 英文</span><span class="sxs-lookup"><span data-stu-id="38b5d-118">IME\_KHOTKEY\_ENGLISH</span></span>             | <span data-ttu-id="38b5d-119"> (韓文) 切換為英文。</span><span class="sxs-lookup"><span data-stu-id="38b5d-119">(Korean) Switch to English.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="38b5d-120">IME \_ KHOTKEY \_ 圖形 \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-120">IME\_KHOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="38b5d-121"> (韓文) 切換 IME 的圖形轉換模式。</span><span class="sxs-lookup"><span data-stu-id="38b5d-121">(Korean) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                                       |
| <span data-ttu-id="38b5d-122">IME \_ KHOTKEY \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="38b5d-122">IME\_KHOTKEY\_HANJACONVERT</span></span>        | <span data-ttu-id="38b5d-123"> (韓文) 切換至 [漢字轉換]。</span><span class="sxs-lookup"><span data-stu-id="38b5d-123">(Korean) Switch to Hanja conversion.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="38b5d-124">輸入法 \_ THOTKEY \_ IME \_ NONIME \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-124">IME\_THOTKEY\_IME\_NONIME\_TOGGLE</span></span> | <span data-ttu-id="38b5d-125">當語言是繁體中文時， (繁體中文) 在輸入法和非 IME 作業之間切換。</span><span class="sxs-lookup"><span data-stu-id="38b5d-125">(Traditional Chinese) Toggle between IME and non-IME operation when the language is Traditional Chinese.</span></span>                                                                                                |
| <span data-ttu-id="38b5d-126">IME \_ THOTKEY \_ 圖形 \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-126">IME\_THOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="38b5d-127"> (繁體中文) 切換 IME 的圖形轉換模式。</span><span class="sxs-lookup"><span data-stu-id="38b5d-127">(Traditional Chinese) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                          |
| <span data-ttu-id="38b5d-128">IME \_ THOTKEY \_ 符號 \_ 切換</span><span class="sxs-lookup"><span data-stu-id="38b5d-128">IME\_THOTKEY\_SYMBOL\_TOGGLE</span></span>      | <span data-ttu-id="38b5d-129"> (繁體中文) 切換 IME 的符號轉換模式。</span><span class="sxs-lookup"><span data-stu-id="38b5d-129">(Traditional Chinese) Toggle the symbol conversion mode of IME.</span></span>                                                                                                                                         |



 

 

 



