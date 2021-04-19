---
description: 從 Windows Server 2008 開始，伺服器功能提供者會提供在伺服器上安裝哪些伺服器功能的相關資訊。 此類別可讓系統管理員清查及管理其伺服器角色和功能。
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: 伺服器功能提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977361"
---
# <a name="server-feature-provider"></a><span data-ttu-id="3205d-104">伺服器功能提供者</span><span class="sxs-lookup"><span data-stu-id="3205d-104">Server Feature Provider</span></span>

<span data-ttu-id="3205d-105">從 Windows Server 2008 開始，伺服器功能提供者會提供在伺服器上安裝哪些伺服器功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3205d-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="3205d-106">此類別可讓系統管理員清查及管理其伺服器角色和功能。</span><span class="sxs-lookup"><span data-stu-id="3205d-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="3205d-107">伺服器角色定義為一組元件，可提供特定功能區域的函式，例如列印、檔案、網域控制項等等。</span><span class="sxs-lookup"><span data-stu-id="3205d-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="3205d-108">一般伺服器角色是檔案伺服器、郵件伺服器、DNS 伺服器、網域控制站、應用程式伺服器等等。</span><span class="sxs-lookup"><span data-stu-id="3205d-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="3205d-109">如果企業未執行報表伺服器角色的管理軟體（例如已安裝管理元件 Microsoft Operations Manager），則您可以藉由查詢 [**Win32 \_ ServerFeature**](win32-serverfeature.md) 類別來取得該資訊。</span><span class="sxs-lookup"><span data-stu-id="3205d-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="3205d-110">遠端電腦上的伺服器角色和功能資訊可透過一般的 WMI 遠端連線或使用 Windows 遠端管理 (WinRM) 服務來取得。</span><span class="sxs-lookup"><span data-stu-id="3205d-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="3205d-111">如需遠端 WMI DCOM 連接的詳細資訊，請參閱 [連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="3205d-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="3205d-112">如需使用 [*ws-management*](/windows/desktop/WinRM/windows-remote-management-glossary) 通訊協定連接的詳細資訊，請參閱 [Windows 遠端管理](/windows/desktop/WinRM/portal)。</span><span class="sxs-lookup"><span data-stu-id="3205d-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="3205d-113">伺服器功能提供者支援下列 WMI 類別：</span><span class="sxs-lookup"><span data-stu-id="3205d-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="3205d-114">**Win32 \_ ServerFeature**</span><span class="sxs-lookup"><span data-stu-id="3205d-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="3205d-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="3205d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3205d-116">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="3205d-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
