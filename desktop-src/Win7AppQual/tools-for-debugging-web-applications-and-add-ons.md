---
description: .
ms.assetid: ECE4A9C6-8553-4718-AAFA-AC4D9924A786
title: 用於調試 Web 應用程式和 Add-Ons 的工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb68485cd674266235d430d7d26b9a39e6fbec14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998176"
---
# <a name="tools-for-debugging-web-applications-and-add-ons"></a><span data-ttu-id="c1323-103">用於調試 Web 應用程式和 Add-Ons 的工具</span><span class="sxs-lookup"><span data-stu-id="c1323-103">Tools for Debugging Web Applications and Add-Ons</span></span>

<span data-ttu-id="c1323-104">您可以將您的程式碼撰寫至最新的 web 標準，而不是 [修正 web 應用程式和附加元件中的相容性問題](remediating-web-applications-and-add-ons.md)，而是讓 web 應用程式或網站以原生方式在 Windows Internet Explorer 8 標準模式下運作。</span><span class="sxs-lookup"><span data-stu-id="c1323-104">Instead of [fixing compatibility issues in web applications and add-ons](remediating-web-applications-and-add-ons.md), you can make the web application or website work natively in Windows Internet Explorer 8 standards mode by writing your code to the most recent web standards.</span></span>

<span data-ttu-id="c1323-105">若要完整評估您的應用程式或網站中的任何問題，您應該研究問題的根本原因。</span><span class="sxs-lookup"><span data-stu-id="c1323-105">To fully assess any problems in your application or website, you should research the root cause of the problem.</span></span> <span data-ttu-id="c1323-106">例如，Internet Explorer 團隊使用開發人員工具判斷根本原因，並以邏輯方式減少可能的問題。</span><span class="sxs-lookup"><span data-stu-id="c1323-106">For example, the Internet Explorer team determined root causes by using the Developer Tools and logically reducing possible issues.</span></span> <span data-ttu-id="c1323-107">下列各節將說明數個可協助簡化偵錯工具的工具。</span><span class="sxs-lookup"><span data-stu-id="c1323-107">The following sections describe several tools to help simplify the debugging process.</span></span>



| <span data-ttu-id="c1323-108">區段</span><span class="sxs-lookup"><span data-stu-id="c1323-108">Section</span></span>                                                                                                                    | <span data-ttu-id="c1323-109">描述</span><span class="sxs-lookup"><span data-stu-id="c1323-109">Description</span></span>                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1323-110">Microsoft Expression Web SuperPreview</span><span class="sxs-lookup"><span data-stu-id="c1323-110">Microsoft Expression Web SuperPreview</span></span>](microsoft-expression-web-superpreview.md)                                         | <span data-ttu-id="c1323-111">獨立的視覺化偵錯工具，可讓您更快速且更輕鬆地將您的網站從 Microsoft Internet Explorer 6 遷移至 Windows Internet Explorer 7 或 Internet Explorer 8。</span><span class="sxs-lookup"><span data-stu-id="c1323-111">A stand-alone visual debugging tool that makes it faster and easier to migrate your sites from Microsoft Internet Explorer 6 to Windows Internet Explorer 7 or Internet Explorer 8.</span></span> |
| [<span data-ttu-id="c1323-112">Internet Explorer 相容性測試工具 (IECTT)</span><span class="sxs-lookup"><span data-stu-id="c1323-112">Internet Explorer Compatibility Test Tool (IECTT)</span></span>](inernet-explorer-compatibility-test-tool--iectt-.md)                  | <span data-ttu-id="c1323-113">[Microsoft 應用程式相容性工具](/windows-hardware/get-started/adk-install)組的元件，可協助您診斷 web 應用程式中的問題。</span><span class="sxs-lookup"><span data-stu-id="c1323-113">A component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install) that can help you diagnose issues in your web applications.</span></span>       |
| [<span data-ttu-id="c1323-114">Internet Explorer 8 開發人員工具</span><span class="sxs-lookup"><span data-stu-id="c1323-114">Internet Explorer 8 Developer Tools</span></span>](internet-explorer-8-developer-tools.md)                                             | <span data-ttu-id="c1323-115">Internet Explorer 8 中包含用於偵錯工具的開發人員工具。</span><span class="sxs-lookup"><span data-stu-id="c1323-115">The developer tools that are included in Internet Explorer 8 for debugging.</span></span>                                                                                                         |
| [<span data-ttu-id="c1323-116">Internet Explorer 8 相容性 Wizard (Aggiorno) </span><span class="sxs-lookup"><span data-stu-id="c1323-116">Internet Explorer 8 Compatibility Wizard (Aggiorno)</span></span>](inernet-explorer-8-compatibility-wizard--aggiorno-.md)              | <span data-ttu-id="c1323-117">協力廠商工具可自動升級網站，以在 Internet Explorer 8 中正確轉譯，而不會中斷舊版瀏覽器的相容性。</span><span class="sxs-lookup"><span data-stu-id="c1323-117">A third-party tool that automatically upgrades websites to render correctly in Internet Explorer 8 without breaking compatibility in older browsers.</span></span>                                |
| [<span data-ttu-id="c1323-118">Fiddler Web 偵錯工具工具</span><span class="sxs-lookup"><span data-stu-id="c1323-118">Fiddler Web Debugger Tool</span></span>](fiddler-web-debugger-tool.md)                                                                 | <span data-ttu-id="c1323-119">用來在網際網路與測試電腦之間捕獲網路流量的協力廠商工具。</span><span class="sxs-lookup"><span data-stu-id="c1323-119">A third-party tool for capturing network traffic between the Internet and test computers.</span></span>                                                                                           |
| [<span data-ttu-id="c1323-120">使用 Virtual PC 映射的應用程式相容性測試</span><span class="sxs-lookup"><span data-stu-id="c1323-120">Application Compatibility Testing Using Virtual PC Images</span></span>](application-compatibility-testing-using-virtual-pc-images.md) | <span data-ttu-id="c1323-121">簡化相容性測試的 Virtual PC 映射。</span><span class="sxs-lookup"><span data-stu-id="c1323-121">Virtual PC images that simplify compatibility testing.</span></span>                                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="c1323-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1323-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1323-123">在遷移至 Internet Explorer 8 時解決應用程式相容性問題</span><span class="sxs-lookup"><span data-stu-id="c1323-123">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
