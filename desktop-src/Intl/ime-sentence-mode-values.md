---
description: 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME 句子模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192981"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="4ff03-103">IME 句子模式值</span><span class="sxs-lookup"><span data-stu-id="4ff03-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="4ff03-104">這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="4ff03-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="4ff03-105">常數</span><span class="sxs-lookup"><span data-stu-id="4ff03-105">Constant</span></span>                  | <span data-ttu-id="4ff03-106">定義</span><span class="sxs-lookup"><span data-stu-id="4ff03-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="4ff03-107">自動輸入法 \_ SMODE \_</span><span class="sxs-lookup"><span data-stu-id="4ff03-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="4ff03-108">IME 會在自動模式中執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="4ff03-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="4ff03-109">IME \_ SMODE \_ 無</span><span class="sxs-lookup"><span data-stu-id="4ff03-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="4ff03-110">沒有句子的資訊。</span><span class="sxs-lookup"><span data-stu-id="4ff03-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="4ff03-111">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="4ff03-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="4ff03-112">IME 會使用片語資訊來預測下一個字元。</span><span class="sxs-lookup"><span data-stu-id="4ff03-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="4ff03-113">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="4ff03-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="4ff03-114">IME 使用複數子句資訊來執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="4ff03-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="4ff03-115">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="4ff03-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="4ff03-116">IME 會以單一字元模式執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="4ff03-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="4ff03-117">IME \_ SMODE \_ 對話</span><span class="sxs-lookup"><span data-stu-id="4ff03-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="4ff03-118">IME 使用交談模式。</span><span class="sxs-lookup"><span data-stu-id="4ff03-118">The IME uses conversation mode.</span></span> <span data-ttu-id="4ff03-119">這對聊天應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="4ff03-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="4ff03-120">Bits 16 到31會保留給 IME 使用。</span><span class="sxs-lookup"><span data-stu-id="4ff03-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



