---
title: 使用遠端桌面服務
description: 如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至網路。
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966396"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="452d9-104">使用遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="452d9-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="452d9-105">下列各節說明如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至 web。</span><span class="sxs-lookup"><span data-stu-id="452d9-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="452d9-106">如果您要尋找遠端桌面連線的使用者資訊，請參閱 [使用遠端桌面連線連接到另一部電腦](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)。</span><span class="sxs-lookup"><span data-stu-id="452d9-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="452d9-107">本主題適用于軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="452d9-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="452d9-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="452d9-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="452d9-109">偵測是否已安裝遠端桌面服務角色</span><span class="sxs-lookup"><span data-stu-id="452d9-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="452d9-110">C # 程式碼範例，其中顯示如果已安裝並執行遠端桌面服務伺服器角色，則會傳回 **True** 的方法，否則從 Windows server 2008 開始會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="452d9-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-111">擴充 Terminal Services Session Broker</span><span class="sxs-lookup"><span data-stu-id="452d9-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="452d9-112">您可以使用 [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM 介面擴充 TS 會話代理人。</span><span class="sxs-lookup"><span data-stu-id="452d9-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-113">執行自訂音訊端點列舉值</span><span class="sxs-lookup"><span data-stu-id="452d9-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="452d9-114">從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。</span><span class="sxs-lookup"><span data-stu-id="452d9-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-115">會話的名字</span><span class="sxs-lookup"><span data-stu-id="452d9-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="452d9-116">分散式 COM (DCOM) 使用系統提供的會話標記，啟用每個會話的物件啟用。</span><span class="sxs-lookup"><span data-stu-id="452d9-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-117">使用遠端桌面服務使用者設定的 ADSI 擴充功能</span><span class="sxs-lookup"><span data-stu-id="452d9-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="452d9-118">您可以使用 Active Directory 服務介面所執行的方法來管理遠端桌面服務特定的使用者屬性， (ADSI) 延伸模組，該擴充功能會與動態連結程式庫 Tsuserex.dll 一起封裝。</span><span class="sxs-lookup"><span data-stu-id="452d9-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-119">使用遠端桌面服務 API</span><span class="sxs-lookup"><span data-stu-id="452d9-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="452d9-120">說明如何使用遠端桌面服務 API，讓應用程式在遠端桌面服務環境中執行工作。</span><span class="sxs-lookup"><span data-stu-id="452d9-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-121">使用遠端桌面虛擬化 API</span><span class="sxs-lookup"><span data-stu-id="452d9-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="452d9-122">開發人員可以使用此 API 來自訂遠端桌面連線代理人 (RD 連線代理人) 用來判斷連入用戶端連線最佳目的地的邏輯。</span><span class="sxs-lookup"><span data-stu-id="452d9-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="452d9-123">自訂 VDI 解決方案的 WSDL 介面</span><span class="sxs-lookup"><span data-stu-id="452d9-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="452d9-124">開發人員可以建立自訂 web 服務，以管理 (VDI) 解決方案的虛擬桌面基礎結構。</span><span class="sxs-lookup"><span data-stu-id="452d9-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="452d9-125">如需詳細資訊，請參閱 [遠端桌面服務程式設計指導方針](terminal-services-programming-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="452d9-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="452d9-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="452d9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="452d9-127">終端機服務現在遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="452d9-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="452d9-128">偵測遠端桌面服務環境</span><span class="sxs-lookup"><span data-stu-id="452d9-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




