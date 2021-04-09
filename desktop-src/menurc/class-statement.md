---
title: CLASS 語句
description: 定義對話方塊的類別。
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- 類別語句功能表和其他資源
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933172"
---
# <a name="class-statement"></a><span data-ttu-id="53b87-104">CLASS 語句</span><span class="sxs-lookup"><span data-stu-id="53b87-104">CLASS statement</span></span>

<span data-ttu-id="53b87-105">定義對話方塊的類別。</span><span class="sxs-lookup"><span data-stu-id="53b87-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="53b87-106">**CLASS** 語句會出現在 [**對話方塊**](dialog-resource.md)語句的 main 之前的選擇性區段中。</span><span class="sxs-lookup"><span data-stu-id="53b87-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="53b87-107">如果未指定任何類別，則會使用標準對話方塊類別。</span><span class="sxs-lookup"><span data-stu-id="53b87-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="53b87-108"><span id="class"></span><span id="CLASS"></span>*類*</span><span class="sxs-lookup"><span data-stu-id="53b87-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="53b87-109">以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。</span><span class="sxs-lookup"><span data-stu-id="53b87-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="53b87-110">如果類別的視窗程式未處理傳送給它的訊息，則必須呼叫 [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) 函式，以確保正確處理所有訊息的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="53b87-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="53b87-111">私用類別可以使用 **DefDlgProc** 做為預設視窗程式。</span><span class="sxs-lookup"><span data-stu-id="53b87-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="53b87-112">類別必須向設定為 **DLGWINDOWEXTRA** 的 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **cbWndExtra** 成員註冊。</span><span class="sxs-lookup"><span data-stu-id="53b87-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53b87-113">備註</span><span class="sxs-lookup"><span data-stu-id="53b87-113">Remarks</span></span>

<span data-ttu-id="53b87-114">**類別** 語句應該只用于特殊的案例，因為它會覆寫對話方塊的正常處理。</span><span class="sxs-lookup"><span data-stu-id="53b87-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="53b87-115">**CLASS** 語句會將對話方塊轉換成指定類別的視窗;這可能會產生非預期的結果，視類別而定。</span><span class="sxs-lookup"><span data-stu-id="53b87-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="53b87-116">請勿使用這個語句所定義的控制項類別名稱。</span><span class="sxs-lookup"><span data-stu-id="53b87-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="53b87-117">範例</span><span class="sxs-lookup"><span data-stu-id="53b87-117">Examples</span></span>

<span data-ttu-id="53b87-118">下列範例示範如何使用 **CLASS** 語句：</span><span class="sxs-lookup"><span data-stu-id="53b87-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="53b87-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53b87-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b87-120">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="53b87-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="53b87-121">**對話 框**</span><span class="sxs-lookup"><span data-stu-id="53b87-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 