---
title: WMI)  (布林值
description: 這是一種 VT \_ BOOL 參數，會採用 variant \_ TRUE (&\# 8211; 1) 或 variant \_ FALSE (0) 的值。
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978310"
---
# <a name="boolean-wmi"></a><span data-ttu-id="7c897-103">WMI)  (布林值</span><span class="sxs-lookup"><span data-stu-id="7c897-103">boolean (WMI)</span></span>

<span data-ttu-id="7c897-104">布林資料類型是一種 VT \_ BOOL 參數，會採用 variant \_ TRUE ( – 1) 或 variant \_ FALSE (0) 的值。</span><span class="sxs-lookup"><span data-stu-id="7c897-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="7c897-105">下表列出 C/c + + 中邏輯 **TRUE** 的程式設計標記法與 Automation 型別之間的差異。</span><span class="sxs-lookup"><span data-stu-id="7c897-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="7c897-106">語言</span><span class="sxs-lookup"><span data-stu-id="7c897-106">Language</span></span>   | <span data-ttu-id="7c897-107">值</span><span class="sxs-lookup"><span data-stu-id="7c897-107">Value</span></span>         | <span data-ttu-id="7c897-108">數值</span><span class="sxs-lookup"><span data-stu-id="7c897-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="7c897-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7c897-109">C/C++</span></span>      | <span data-ttu-id="7c897-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="7c897-110">**TRUE**</span></span>      | <span data-ttu-id="7c897-111">1</span><span class="sxs-lookup"><span data-stu-id="7c897-111">1</span></span>               |
| <span data-ttu-id="7c897-112">自動化</span><span class="sxs-lookup"><span data-stu-id="7c897-112">Automation</span></span> | <span data-ttu-id="7c897-113">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="7c897-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="7c897-114">–1</span><span class="sxs-lookup"><span data-stu-id="7c897-114">–1</span></span>              |

<span data-ttu-id="7c897-115">這兩種類型都是非零，因此不是 **FALSE**，但是有不同的標記法表示為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7c897-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
