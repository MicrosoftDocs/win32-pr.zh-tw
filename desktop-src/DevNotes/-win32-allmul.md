---
title: _allmul 常式
description: 將兩個 LONGLONG 或 ULONGLONG 整數相乘。
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104022955"
---
# <a name="_allmul-routine"></a><span data-ttu-id="fe078-103">\_allmul 常式</span><span class="sxs-lookup"><span data-stu-id="fe078-103">\_allmul Routine</span></span>

<span data-ttu-id="fe078-104">將兩個 **LONGLONG** 或 **ULONGLONG** 整數相乘。</span><span class="sxs-lookup"><span data-stu-id="fe078-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="fe078-105">例如，若要將兩個 int64 值相乘，編譯器可能會產生對 **\_ allmul** 常式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fe078-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe078-106">備註</span><span class="sxs-lookup"><span data-stu-id="fe078-106">Remarks</span></span>

<span data-ttu-id="fe078-107">**\_ Allmul** 常式是 C 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="fe078-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="fe078-108">編譯器是否使用 **\_ allmul** 完全取決於優化集。</span><span class="sxs-lookup"><span data-stu-id="fe078-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="fe078-109">此常式只適用于 x86 平臺。</span><span class="sxs-lookup"><span data-stu-id="fe078-109">This routine is used only on x86 platforms.</span></span>
