---
title: Active Accessibility 和消費者介面自動化
description: Microsoft Active Accessibility 是專為搭配 Windows XP 和舊版作業系統使用所設計。
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966414"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="a97e8-103">Active Accessibility 和消費者介面自動化</span><span class="sxs-lookup"><span data-stu-id="a97e8-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="a97e8-104">Microsoft Active Accessibility 是專為搭配 Windows XP 和舊版作業系統使用所設計。</span><span class="sxs-lookup"><span data-stu-id="a97e8-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="a97e8-105">適用于 Windows XP 和 Windows Vista 的自訂控制項和可存取技術用戶端應用程式的開發人員，應該考慮改為使用 Microsoft [消費者介面自動化](entry-uiauto-win32.md) 。</span><span class="sxs-lookup"><span data-stu-id="a97e8-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="a97e8-106">Microsoft 消費者介面自動化是一種功能完整的系統，可提供更精確的使用者介面相關資訊，並讓使用者更能夠與控制項互動。</span><span class="sxs-lookup"><span data-stu-id="a97e8-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="a97e8-107">尤其是，它提供大幅增強的文字支援。</span><span class="sxs-lookup"><span data-stu-id="a97e8-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="a97e8-108">一組 proxy 物件提供標準 Microsoft Win32 和 Windows Forms 控制項的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="a97e8-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="a97e8-109">更豐富的支援適用于特別以消費者介面自動化撰寫的控制項，包括原生 Windows Presentation Foundation (WPF) 元素，這些專案不會直接支援 Microsoft Active Accessibility。</span><span class="sxs-lookup"><span data-stu-id="a97e8-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="a97e8-110">支援消費者介面自動化的自訂控制項可以撰寫為 managed 或非受控碼。</span><span class="sxs-lookup"><span data-stu-id="a97e8-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="a97e8-111">Microsoft Active Accessibility 的用戶端會透過橋接層存取有限的 UI 元素，僅支援消費者介面自動化。</span><span class="sxs-lookup"><span data-stu-id="a97e8-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="a97e8-112">如需詳細資訊，請參閱 [附錄 G： Active Accessibility 橋接器至消費者介面自動化](appendix-g--active-accessibility-bridge-to-ui-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="a97e8-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="a97e8-113">如需有關 Microsoft Active Accessibility 和消費者介面自動化之間的相似性和差異的詳細資訊，請參閱 [Microsoft Active Accessibility 和消費者介面自動化比較](microsoft-active-accessibility-and-ui-automation-compared.md)。</span><span class="sxs-lookup"><span data-stu-id="a97e8-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a97e8-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a97e8-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a97e8-115">**概念**</span><span class="sxs-lookup"><span data-stu-id="a97e8-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a97e8-116">快速入門</span><span class="sxs-lookup"><span data-stu-id="a97e8-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="a97e8-117">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="a97e8-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




