---
description: Windows Update Agent (WUA) API 是一組 COM 介面，可讓系統管理員和程式設計人員存取 Windows Update 和 Windows Server Update Services (WSUS) 。
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Update 代理程式 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689676"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="45904-103">Windows Update 代理程式 API</span><span class="sxs-lookup"><span data-stu-id="45904-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="45904-104">目的</span><span class="sxs-lookup"><span data-stu-id="45904-104">Purpose</span></span>

<span data-ttu-id="45904-105">Windows Update Agent (WUA) API 是一組 COM 介面，可讓系統管理員和程式設計人員存取 Windows Update 和 [Windows Server Update Services (WSUS) ](/previous-versions/windows/desktop/ms744624(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="45904-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="45904-106">您可以撰寫腳本和程式來檢查目前可供電腦使用的更新，然後您就可以安裝或卸載更新。</span><span class="sxs-lookup"><span data-stu-id="45904-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="45904-107">適用時</span><span class="sxs-lookup"><span data-stu-id="45904-107">Where applicable</span></span>

<span data-ttu-id="45904-108">系統管理員可以使用 WUA，以程式設計方式判斷應該套用至電腦的更新、下載這些更新，然後在幾乎不需要使用者介入的情況下進行安裝。</span><span class="sxs-lookup"><span data-stu-id="45904-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="45904-109">獨立軟體廠商 (ISV) 和使用者開發人員可以將 WUA 功能整合到電腦管理或更新管理軟體，以提供順暢的操作環境。</span><span class="sxs-lookup"><span data-stu-id="45904-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="45904-110">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="45904-110">Developer audience</span></span>

<span data-ttu-id="45904-111">您可以用數種程式設計語言撰寫 WUA 應用程式。</span><span class="sxs-lookup"><span data-stu-id="45904-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="45904-112">WUA 會定義 Visual Basic、Visual Basic Scripting Edition (VBScript) 、JScript 以及 C 和 c + + 可存取的介面和物件。</span><span class="sxs-lookup"><span data-stu-id="45904-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="45904-113">熟悉 COM 程式設計對 WUA 程式設計師很有用。</span><span class="sxs-lookup"><span data-stu-id="45904-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="45904-114">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="45904-114">Run-time requirements</span></span>

<span data-ttu-id="45904-115">從 Windows XP 開始支援 WUA。</span><span class="sxs-lookup"><span data-stu-id="45904-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="45904-116">從 Windows Server 2003 開始，伺服器支援 WUA。</span><span class="sxs-lookup"><span data-stu-id="45904-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="45904-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="45904-117">In this section</span></span>

-   [<span data-ttu-id="45904-118">使用 Windows Update 代理程式 API</span><span class="sxs-lookup"><span data-stu-id="45904-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="45904-119">WUA API 參考</span><span class="sxs-lookup"><span data-stu-id="45904-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
