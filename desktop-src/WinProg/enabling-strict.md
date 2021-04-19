---
title: 啟用 STRICT
description: 當您定義 STRICT 符號時，會啟用在宣告和使用類型時需要更多注意的功能。
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106974744"
---
# <a name="enabling-strict"></a><span data-ttu-id="88607-103">啟用 STRICT</span><span class="sxs-lookup"><span data-stu-id="88607-103">Enabling STRICT</span></span>

<span data-ttu-id="88607-104">當您定義 **STRICT** 符號時，會啟用在宣告和使用類型時需要更多注意的功能。</span><span class="sxs-lookup"><span data-stu-id="88607-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="88607-105">這可協助您撰寫更多可移植的程式碼。</span><span class="sxs-lookup"><span data-stu-id="88607-105">This helps you write more portable code.</span></span> <span data-ttu-id="88607-106">這種額外的小心也會減少您的調試時間。</span><span class="sxs-lookup"><span data-stu-id="88607-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="88607-107">啟用 **STRICT** 會重新定義某些資料類型，讓編譯器不允許在沒有明確轉換的情況下，從某個類型指派給另一個類型。</span><span class="sxs-lookup"><span data-stu-id="88607-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="88607-108">這對 Windows 程式碼特別有用。</span><span class="sxs-lookup"><span data-stu-id="88607-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="88607-109">傳遞資料類型的錯誤會在編譯時期報告，而不會在執行時間造成嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="88607-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="88607-110">使用 Visual C++，預設會定義 **嚴格** 的類型檢查。</span><span class="sxs-lookup"><span data-stu-id="88607-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="88607-111">若要定義逐檔案的 **STRICT** ，請在包含 Windows .h 之前插入 **\# define** 語句：</span><span class="sxs-lookup"><span data-stu-id="88607-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="88607-112">當定義 **STRICT** 時， [資料類型](windows-data-types.md) 定義會變更，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88607-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="88607-113">特定的控制碼類型已定義為互斥;例如，您將無法在需要 **HDC** 型別引數的情況下傳遞 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="88607-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="88607-114">如果沒有 **STRICT**，所有控制碼都會定義為 **控制碼**，因此編譯器不會防止您使用某種類型的控制碼，也就是預期的另一種類型。</span><span class="sxs-lookup"><span data-stu-id="88607-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="88607-115">所有的回呼函數類型 (例如對話方塊程式、視窗程式和攔截程式) 都會以完整原型定義。</span><span class="sxs-lookup"><span data-stu-id="88607-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="88607-116">這可防止您以不正確的參數清單宣告回呼函數。</span><span class="sxs-lookup"><span data-stu-id="88607-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="88607-117">應使用泛型指標的參數和傳回值型別，會正確宣告為 **LPVOID** ，而不是 **LPSTR** 或其他指標類型。</span><span class="sxs-lookup"><span data-stu-id="88607-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="88607-118">[**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat)結構是根據 ANSI 標準來宣告。</span><span class="sxs-lookup"><span data-stu-id="88607-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88607-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="88607-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88607-120">停用 STRICT</span><span class="sxs-lookup"><span data-stu-id="88607-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="88607-121">嚴格合規性</span><span class="sxs-lookup"><span data-stu-id="88607-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
