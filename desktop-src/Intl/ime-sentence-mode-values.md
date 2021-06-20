---
description: 查看輸入法編輯器 (IME) 句子模式值的清單。 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME 句子模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406761"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="e0512-104">IME 句子模式值</span><span class="sxs-lookup"><span data-stu-id="e0512-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="e0512-105">這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="e0512-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="e0512-106">常數</span><span class="sxs-lookup"><span data-stu-id="e0512-106">Constant</span></span>                  | <span data-ttu-id="e0512-107">定義</span><span class="sxs-lookup"><span data-stu-id="e0512-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e0512-108">自動輸入法 \_ SMODE \_</span><span class="sxs-lookup"><span data-stu-id="e0512-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="e0512-109">IME 會在自動模式中執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="e0512-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="e0512-110">IME \_ SMODE \_ 無</span><span class="sxs-lookup"><span data-stu-id="e0512-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="e0512-111">沒有句子的資訊。</span><span class="sxs-lookup"><span data-stu-id="e0512-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="e0512-112">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="e0512-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="e0512-113">IME 會使用片語資訊來預測下一個字元。</span><span class="sxs-lookup"><span data-stu-id="e0512-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="e0512-114">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="e0512-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="e0512-115">IME 使用複數子句資訊來執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="e0512-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="e0512-116">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="e0512-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="e0512-117">IME 會以單一字元模式執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="e0512-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="e0512-118">IME \_ SMODE \_ 對話</span><span class="sxs-lookup"><span data-stu-id="e0512-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="e0512-119">IME 使用交談模式。</span><span class="sxs-lookup"><span data-stu-id="e0512-119">The IME uses conversation mode.</span></span> <span data-ttu-id="e0512-120">這對聊天應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="e0512-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="e0512-121">Bits 16 到31會保留給 IME 使用。</span><span class="sxs-lookup"><span data-stu-id="e0512-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



