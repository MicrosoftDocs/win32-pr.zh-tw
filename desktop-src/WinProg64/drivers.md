---
title: 64位 Windows) 的驅動程式 (程式設計指南
description: Windows 64 位版本的設計目的，是為了讓開發人員可以針對其32位和64位應用程式使用單一的原始程式碼基底程式碼基底。 在很大的程度上，這也適用于32位和64位的 Windows 驅動程式。
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- 驅動程式64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317060"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="0956e-105">64位 Windows) 的驅動程式 (程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0956e-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="0956e-106">Windows 64 位版本的設計目的，是為了讓開發人員可以針對其32位和64位應用程式使用單一的原始程式碼基底程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="0956e-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="0956e-107">在很大的程度上，這也適用于32位和64位的 Windows 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0956e-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="0956e-108">但是，32位驅動程式無法在64位的 Windows 上執行，而且必須進行移植。</span><span class="sxs-lookup"><span data-stu-id="0956e-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="0956e-109">針對使用者模式應用程式，64位 Windows 包含 WOW64，可讓32位 Windows 應用程式執行 (，並在執行64位 Windows 的系統上) 某些效能降低。</span><span class="sxs-lookup"><span data-stu-id="0956e-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="0956e-110">驅動程式沒有對等的轉譯層存在。</span><span class="sxs-lookup"><span data-stu-id="0956e-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="0956e-111">如需將驅動程式移植到64位 Windows 的相關資訊，請參閱 Windows 驅動程式套件 (WDK) 中的 [64 位問題](https://msdn.microsoft.com/library/aa489627.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="0956e-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




