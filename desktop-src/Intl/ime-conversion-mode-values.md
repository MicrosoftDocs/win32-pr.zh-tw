---
description: 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: IME 轉換模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113624"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="7a0f4-103">IME 轉換模式值</span><span class="sxs-lookup"><span data-stu-id="7a0f4-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="7a0f4-104">這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="7a0f4-105">bit</span><span class="sxs-lookup"><span data-stu-id="7a0f4-105">Bit</span></span>                      | <span data-ttu-id="7a0f4-106">意義</span><span class="sxs-lookup"><span data-stu-id="7a0f4-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0f4-107">IME \_ CMODE 英 \_ 數位元</span><span class="sxs-lookup"><span data-stu-id="7a0f4-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="7a0f4-108">英數位元輸入模式。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-108">Alphanumeric input mode.</span></span> <span data-ttu-id="7a0f4-109">這是預設值，定義為0x0000。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="7a0f4-110">IME \_ CMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="7a0f4-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="7a0f4-111">如果字元碼輸入模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="7a0f4-112">輸入法 \_ CMODE \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="7a0f4-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="7a0f4-113">如果 EUDC 轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="7a0f4-114">輸入法 \_ CMODE \_ 固定</span><span class="sxs-lookup"><span data-stu-id="7a0f4-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="7a0f4-115">**Windows Me/98、windows 2000、WINDOWS XP：** 如果固定的轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="7a0f4-116">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="7a0f4-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="7a0f4-117">如果全圖形模式，則設定為 1;如果為半形狀模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="7a0f4-118">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="7a0f4-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="7a0f4-119">如果是漢字轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="7a0f4-120">輸入法 \_ CMODE \_ 片假名</span><span class="sxs-lookup"><span data-stu-id="7a0f4-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="7a0f4-121">若為片假名模式，則設定為 1;若為平假名模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="7a0f4-122">IME \_ CMODE \_ 原生</span><span class="sxs-lookup"><span data-stu-id="7a0f4-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="7a0f4-123">如果原生模式，則設定為 1;若為英數位元模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="7a0f4-124">IME \_ CMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="7a0f4-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="7a0f4-125">設定為1以防止依 IME 處理轉換;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="7a0f4-126">IME \_ CMODE \_ 羅馬</span><span class="sxs-lookup"><span data-stu-id="7a0f4-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="7a0f4-127">如果羅馬字輸入模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="7a0f4-128">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="7a0f4-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="7a0f4-129">如果軟鍵盤模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="7a0f4-130">IME \_ CMODE \_ 符號</span><span class="sxs-lookup"><span data-stu-id="7a0f4-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="7a0f4-131">如果符號轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="7a0f4-132">所有其他位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-132">All other bits are reserved.</span></span>

 

 



