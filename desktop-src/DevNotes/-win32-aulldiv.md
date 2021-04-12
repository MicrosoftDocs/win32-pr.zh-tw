---
title: _aulldiv 常式
description: 將兩個 ULONGLONG 整數相除。
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104462688"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="71bc1-103">\_aulldiv 常式</span><span class="sxs-lookup"><span data-stu-id="71bc1-103">\_aulldiv Routine</span></span>

<span data-ttu-id="71bc1-104">將兩個 **ULONGLONG** 整數相除。</span><span class="sxs-lookup"><span data-stu-id="71bc1-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="71bc1-105">例如，若要將兩個 uint64 值相除，編譯器可能會產生對 **\_ aulldiv** 常式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="71bc1-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="71bc1-106">備註</span><span class="sxs-lookup"><span data-stu-id="71bc1-106">Remarks</span></span>

<span data-ttu-id="71bc1-107">**\_ Aulldiv** 常式是 C 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="71bc1-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="71bc1-108">編譯器是否使用 **\_ aulldiv** 完全取決於優化集。</span><span class="sxs-lookup"><span data-stu-id="71bc1-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="71bc1-109">此函式僅適用于 x86 平臺。</span><span class="sxs-lookup"><span data-stu-id="71bc1-109">This function is used only on x86 platforms.</span></span>
