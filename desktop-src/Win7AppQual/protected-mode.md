---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: 受保護模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849851"
---
# <a name="protected-mode"></a><span data-ttu-id="c1846-103">受保護模式</span><span class="sxs-lookup"><span data-stu-id="c1846-103">Protected Mode</span></span>

<span data-ttu-id="c1846-104">在 Windows XP Service Pack 2 (SP2) 作業系統和更新版本的 Internet Explorer 8 中，大部分的 Windows Internet Explorer 8 安全性功能都有提供。</span><span class="sxs-lookup"><span data-stu-id="c1846-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="c1846-105">受保護模式僅適用于 Windows Vista 或更新版本，因為它是以 Windows Vista 的新功能為基礎：</span><span class="sxs-lookup"><span data-stu-id="c1846-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="c1846-106">[ (UAC) 的使用者帳戶控制 ](https://msdn.microsoft.com/library/aa511445.aspx) 可讓您在沒有系統管理員許可權的情況下輕鬆執行。</span><span class="sxs-lookup"><span data-stu-id="c1846-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="c1846-107">當使用者以有限的使用者權限執行程式時，攻擊者會比使用系統管理員許可權執行的程式更安全。</span><span class="sxs-lookup"><span data-stu-id="c1846-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="c1846-108">Windows 作業系統可以限制惡意程式碼免于執行損害的動作。</span><span class="sxs-lookup"><span data-stu-id="c1846-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="c1846-109">完整性機制會以較低完整性的程式限制對 [安全物件](../secauthz/securable-objects.md) 的寫入存取權，就像使用者帳戶群組成員資格限制使用者存取機密系統元件的許可權一樣。</span><span class="sxs-lookup"><span data-stu-id="c1846-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="c1846-110">[消費者介面許可權隔離 (UIPI) ](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) 可防止進程將選取的視窗訊息和其他使用者 api 傳送至以較高完整性執行的進程。</span><span class="sxs-lookup"><span data-stu-id="c1846-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="c1846-111">Windows 整合機制安全性基礎結構可讓受保護模式為 Windows Internet Explorer 提供使用者流覽 web 所需的許可權，以及使用者需要以無訊息模式安裝程式或修改機密系統資料的必要許可權。</span><span class="sxs-lookup"><span data-stu-id="c1846-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="c1846-112">使用者可以透過核取方塊停用這項功能，系統管理員可以使用群組原則來停用此功能。</span><span class="sxs-lookup"><span data-stu-id="c1846-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1846-113">在進行疑難排解時，您應該只將此功能停用為暫時量值，以在功能啟用時比較應用程式的行為。</span><span class="sxs-lookup"><span data-stu-id="c1846-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="c1846-114">建議您將此功能永久啟用。</span><span class="sxs-lookup"><span data-stu-id="c1846-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c1846-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1846-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1846-116">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="c1846-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
