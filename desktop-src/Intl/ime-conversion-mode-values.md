---
description: 查看輸入法編輯器 (IME) 轉換模式值的清單。 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: IME 轉換模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406751"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="cce64-104">IME 轉換模式值</span><span class="sxs-lookup"><span data-stu-id="cce64-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="cce64-105">這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="cce64-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="cce64-106">bit</span><span class="sxs-lookup"><span data-stu-id="cce64-106">Bit</span></span>                      | <span data-ttu-id="cce64-107">意義</span><span class="sxs-lookup"><span data-stu-id="cce64-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce64-108">IME \_ CMODE 英 \_ 數位元</span><span class="sxs-lookup"><span data-stu-id="cce64-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="cce64-109">英數位元輸入模式。</span><span class="sxs-lookup"><span data-stu-id="cce64-109">Alphanumeric input mode.</span></span> <span data-ttu-id="cce64-110">這是預設值，定義為0x0000。</span><span class="sxs-lookup"><span data-stu-id="cce64-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="cce64-111">IME \_ CMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="cce64-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="cce64-112">如果字元碼輸入模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="cce64-113">輸入法 \_ CMODE \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="cce64-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="cce64-114">如果 EUDC 轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="cce64-115">輸入法 \_ CMODE \_ 固定</span><span class="sxs-lookup"><span data-stu-id="cce64-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="cce64-116">**Windows Me/98、windows 2000、WINDOWS XP：** 如果固定的轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="cce64-117">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="cce64-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="cce64-118">如果全圖形模式，則設定為 1;如果為半形狀模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="cce64-119">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="cce64-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="cce64-120">如果是漢字轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="cce64-121">輸入法 \_ CMODE \_ 片假名</span><span class="sxs-lookup"><span data-stu-id="cce64-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="cce64-122">若為片假名模式，則設定為 1;若為平假名模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="cce64-123">IME \_ CMODE \_ 原生</span><span class="sxs-lookup"><span data-stu-id="cce64-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="cce64-124">如果原生模式，則設定為 1;若為英數位元模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="cce64-125">IME \_ CMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="cce64-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="cce64-126">設定為1以防止依 IME 處理轉換;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="cce64-127">IME \_ CMODE \_ 羅馬</span><span class="sxs-lookup"><span data-stu-id="cce64-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="cce64-128">如果羅馬字輸入模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="cce64-129">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="cce64-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="cce64-130">如果軟鍵盤模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="cce64-131">IME \_ CMODE \_ 符號</span><span class="sxs-lookup"><span data-stu-id="cce64-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="cce64-132">如果符號轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="cce64-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="cce64-133">所有其他位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="cce64-133">All other bits are reserved.</span></span>

 

 



