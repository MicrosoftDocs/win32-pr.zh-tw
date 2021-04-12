---
title: 準備開始64位 Windows
description: Windows 64 位版本的主要目標是讓開發人員輕鬆地針對其32位和64位應用程式使用單一原始程式碼基底。
ms.assetid: 62101e20-13bb-46d5-9542-2afd414ad224
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，做好準備
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b585f2798650f84930e6aa2e5d6e19cb9aa5e8e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382469"
---
# <a name="getting-ready-for-64-bit-windows"></a><span data-ttu-id="99238-104">準備開始64位 Windows</span><span class="sxs-lookup"><span data-stu-id="99238-104">Getting Ready for 64-bit Windows</span></span>

<span data-ttu-id="99238-105">Windows 64 位版本的主要目標是讓開發人員輕鬆地針對其32位和64位應用程式使用單一原始程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="99238-105">A key goal of the 64-bit version of Windows is to make it easy for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="99238-106">本總覽說明如何讓您的原始程式碼同時支援32位和64位運算。</span><span class="sxs-lookup"><span data-stu-id="99238-106">This overview describes how to make your source code support both 32-bit and 64-bit computing.</span></span> <span data-ttu-id="99238-107">熟悉現有的 [Windows 資料類型](/windows/desktop/WinProg/windows-data-types) 將有所説明。</span><span class="sxs-lookup"><span data-stu-id="99238-107">Familiarity with existing [Windows data types](/windows/desktop/WinProg/windows-data-types) will help.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99238-108">本章節內容</span><span class="sxs-lookup"><span data-stu-id="99238-108">In this Section</span></span>

-   [<span data-ttu-id="99238-109">抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="99238-109">Abstract Data Models</span></span>](abstract-data-models.md)
-   [<span data-ttu-id="99238-110">新的資料類型</span><span class="sxs-lookup"><span data-stu-id="99238-110">The New Data Types</span></span>](the-new-data-types.md)
-   [<span data-ttu-id="99238-111">環境</span><span class="sxs-lookup"><span data-stu-id="99238-111">The Environment</span></span>](the-environment.md)
-   [<span data-ttu-id="99238-112">工具</span><span class="sxs-lookup"><span data-stu-id="99238-112">The Tools</span></span>](the-tools.md)
-   [<span data-ttu-id="99238-113">使用指標的規則</span><span class="sxs-lookup"><span data-stu-id="99238-113">Rules for Using Pointers</span></span>](rules-for-using-pointers.md)
-   [<span data-ttu-id="99238-114">虛擬位址空間</span><span class="sxs-lookup"><span data-stu-id="99238-114">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="99238-115">對齊錯誤</span><span class="sxs-lookup"><span data-stu-id="99238-115">Alignment Faults</span></span>](fault-alignments.md)
-   [<span data-ttu-id="99238-116">進程互通性</span><span class="sxs-lookup"><span data-stu-id="99238-116">Process Interoperability</span></span>](process-interoperability.md)
-   [<span data-ttu-id="99238-117">驅動程式</span><span class="sxs-lookup"><span data-stu-id="99238-117">Drivers</span></span>](drivers.md)

 

 