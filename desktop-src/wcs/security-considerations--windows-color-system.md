---
title: 安全性考慮 Windows 色彩系統
description: 安全性考慮 Windows 色彩系統
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Color System (WCS) ，安全性
- WCS (Windows 色彩系統) ，安全性
- 影像色彩管理，安全性
- 色彩管理，安全性
- Windows Color System (WCS) 的安全性
- '色彩管理模組 (CMM) '
- " (色彩管理模組) 的 CMM"
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992239"
---
# <a name="security-considerations-windows-color-system"></a><span data-ttu-id="0cfa5-110">安全性考慮： Windows 色彩系統</span><span class="sxs-lookup"><span data-stu-id="0cfa5-110">Security Considerations: Windows Color System</span></span>

<span data-ttu-id="0cfa5-111">本檔提供與影像色彩管理相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="0cfa5-111">This document provides information about security considerations related to image color management.</span></span> <span data-ttu-id="0cfa5-112">本檔並不提供您需要瞭解的安全性問題，而是使用它作為此技術領域的起點和參考。</span><span class="sxs-lookup"><span data-stu-id="0cfa5-112">This document doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

## <a name="non-microsoft-cmms-can-run-in-system-context"></a><span data-ttu-id="0cfa5-113">非 Microsoft Cmm 可以在系統內容中執行</span><span class="sxs-lookup"><span data-stu-id="0cfa5-113">Non-Microsoft CMMs can run in system context</span></span>

<span data-ttu-id="0cfa5-114">非 Microsoft 色彩管理模組 (Cmm) 應該視為非 Microsoft 印表機驅動程式，因為它們有可能在系統內容中執行，以進行列印工作。</span><span class="sxs-lookup"><span data-stu-id="0cfa5-114">Non-Microsoft Color Management Modules (CMMs) should be treated like non-Microsoft printer drivers because they have the potential to run in a system context for printing operations.</span></span>
