---
title: Windows Automation API 總覽
description: Microsoft Windows 提供兩種 API 規格，適用于使用者介面的協助工具和軟體測試自動化 Microsoft Active Accessibility 以及 Microsoft 消費者介面自動化。
ms.assetid: 73acc580-9573-40ea-8727-b0e7292b2a4c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac67c5311d0d936e45235c527ebb15c238ba808
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315658"
---
# <a name="windows-accessibility-api-overview"></a><span data-ttu-id="f8ab2-103">Windows 協助工具 API 總覽</span><span class="sxs-lookup"><span data-stu-id="f8ab2-103">Windows Accessibility API overview</span></span>

<span data-ttu-id="f8ab2-104">本節提供 Microsoft Windows Automation API 3.0 的高階總覽和詳細 API 參考，其中包括 Microsoft [消費者介面自動化規格](./uiauto-specandcommunitypromise.md)的 Windows 執行，以及在 windows 95 中引進的 Microsoft Active Accessibility (舊版功能，以作為平臺的增益集) 。</span><span class="sxs-lookup"><span data-stu-id="f8ab2-104">This section provides high-level overviews and detailed API reference for both the Microsoft Windows Automation API 3.0, which includes the Windows implementation of the Microsoft [UI Automation Specification](./uiauto-specandcommunitypromise.md), and Microsoft Active Accessibility (legacy feature introduced in Windows 95 as a platform add-in).</span></span>

<span data-ttu-id="f8ab2-105">我們會說明 Microsoft Active Accessibility 和消費者介面自動化之間的相似性和差異，這兩種技術可搭配使用，並提供指導方針，讓您選擇要針對特定案例執行的技術。</span><span class="sxs-lookup"><span data-stu-id="f8ab2-105">We describe the similarities and differences between Microsoft Active Accessibility and UI Automation, the components and features that enable the two technologies to work together, and provide guidelines for choosing which technology to implement for your specific scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8ab2-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8ab2-106">Related topics</span></span>

[<span data-ttu-id="f8ab2-107">消費者介面自動化的社會承諾</span><span class="sxs-lookup"><span data-stu-id="f8ab2-107">UI Automation Community Promise</span></span>](./uiauto-specandcommunitypromise.md)