---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) 的安全性 (
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195570"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="e7d08-103">Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) 的安全性 (</span><span class="sxs-lookup"><span data-stu-id="e7d08-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="e7d08-104">從 Windows Internet Explorer 7 開始，當使用者在 Windows Vista 作業系統或更新版本上執行時，Windows Internet Explorer 就會在稱為 *受保護模式* 的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="e7d08-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="e7d08-105">這種模式會以比標準使用者應用程式低的許可權設定來執行 Internet Explorer，因此某些功能會受到限制，尤其是 ActiveX 控制項和特定類型的外掛程式。如需 Internet Explorer 中受保護模式的詳細資訊及其對相容性的影響，請參閱 MSDN Library 中的 [瞭解和使用受保護模式 Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) 。</span><span class="sxs-lookup"><span data-stu-id="e7d08-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="e7d08-106">Windows Internet Explorer 8 預設也會啟用資料執行防止 (DEP) ，以協助應用程式避免在線上攻擊中執行任意程式碼。</span><span class="sxs-lookup"><span data-stu-id="e7d08-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="e7d08-107">不過，某些附加元件可能不會使用這項安全性功能 (例如，任何未設計為只執行記憶體中已明確標示為可執行檔的程式碼的附加元件，例如使用舊版 ActiveX 範本程式庫所建立的應用程式， (ATL) framework) 。</span><span class="sxs-lookup"><span data-stu-id="e7d08-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="e7d08-108">Internet Explorer 8 也可保護使用者免于使用腳本的潛在安全性漏洞。</span><span class="sxs-lookup"><span data-stu-id="e7d08-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="e7d08-109">例如，除非透過明確的使用者互動，否則您無法從較不受信任區域中的 URL 流覽至更受信任區域中的 URL。</span><span class="sxs-lookup"><span data-stu-id="e7d08-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="e7d08-110">您也無法隱藏瀏覽器使用者介面的特定元素 (例如，在不受信任的 (網際網路) 區域中的 [網址列]) 。</span><span class="sxs-lookup"><span data-stu-id="e7d08-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7d08-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7d08-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d08-112">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="e7d08-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
