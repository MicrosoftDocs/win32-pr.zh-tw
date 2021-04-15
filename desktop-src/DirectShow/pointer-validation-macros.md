---
description: 指標驗證宏
ms.assetid: 53b080ba-d8cf-48a3-a895-2c14d54f7e21
title: 指標驗證宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dadf5fd2df1e4f7568d899ff93d4a401404830f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467693"
---
# <a name="pointer-validation-macros"></a><span data-ttu-id="24465-103">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="24465-103">Pointer Validation Macros</span></span>

<span data-ttu-id="24465-104">Microsoft DirectShow 提供數個宏來驗證指標。</span><span class="sxs-lookup"><span data-stu-id="24465-104">Microsoft DirectShow provides several macros for validating pointers.</span></span>



| <span data-ttu-id="24465-105">巨集</span><span class="sxs-lookup"><span data-stu-id="24465-105">Macro</span></span>                                                | <span data-ttu-id="24465-106">Description</span><span class="sxs-lookup"><span data-stu-id="24465-106">Description</span></span>                                                                   |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="24465-107">**CheckPointer**</span><span class="sxs-lookup"><span data-stu-id="24465-107">**CheckPointer**</span></span>](checkpointer.md)                 | <span data-ttu-id="24465-108">檢查指標是否為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="24465-108">Checks whether a pointer is **NULL**.</span></span>                                         |
| [<span data-ttu-id="24465-109">**ValidateReadPtr**</span><span class="sxs-lookup"><span data-stu-id="24465-109">**ValidateReadPtr**</span></span>](validatereadptr.md)           | <span data-ttu-id="24465-110">確認呼叫進程具有記憶體區塊的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="24465-110">Verifies that the calling process has read access to a memory block.</span></span>          |
| [<span data-ttu-id="24465-111">**ValidateReadWritePtr**</span><span class="sxs-lookup"><span data-stu-id="24465-111">**ValidateReadWritePtr**</span></span>](validatereadwriteptr.md) | <span data-ttu-id="24465-112">確認呼叫進程具有記憶體區塊的讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="24465-112">Verifies that the calling process has read/write access to a memory block.</span></span>    |
| [<span data-ttu-id="24465-113">**ValidateStringPtr**</span><span class="sxs-lookup"><span data-stu-id="24465-113">**ValidateStringPtr**</span></span>](validatestringptr.md)       | <span data-ttu-id="24465-114">確認呼叫進程具有字串的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="24465-114">Verifies that the calling process has read access to a string.</span></span>                |
| [<span data-ttu-id="24465-115">**ValidateStringPtrA**</span><span class="sxs-lookup"><span data-stu-id="24465-115">**ValidateStringPtrA**</span></span>](validatestringptra.md)     | <span data-ttu-id="24465-116">確認呼叫進程具有 ANSI 字串的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="24465-116">Verifies that the calling process has read access to an ANSI string.</span></span>          |
| [<span data-ttu-id="24465-117">**ValidateStringPtrW**</span><span class="sxs-lookup"><span data-stu-id="24465-117">**ValidateStringPtrW**</span></span>](validatestringptrw.md)     | <span data-ttu-id="24465-118">確認呼叫進程具有寬字元字串的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="24465-118">Verifies that the calling process has read access to a wide-character string.</span></span> |
| [<span data-ttu-id="24465-119">**ValidateWritePtr**</span><span class="sxs-lookup"><span data-stu-id="24465-119">**ValidateWritePtr**</span></span>](validatewriteptr.md)         | <span data-ttu-id="24465-120">確認呼叫進程具有記憶體區塊的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="24465-120">Verifies that the calling process has write access to a memory block.</span></span>         |



 

 

 



