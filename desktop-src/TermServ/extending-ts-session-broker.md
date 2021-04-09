---
title: 擴充 Terminal Services Session Broker
description: 您可以擴充 TS \ 160;使用 IWTSSBPlugin COM 介面的會話代理程式。
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682855"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="e6c15-103">擴充 Terminal Services Session Broker</span><span class="sxs-lookup"><span data-stu-id="e6c15-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="e6c15-104">終端機服務會話代理人 (「TS 會話代理人」) 判斷起始連接的使用者是否已開啟會話。</span><span class="sxs-lookup"><span data-stu-id="e6c15-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="e6c15-105">如果是，TS 會話代理人會將連入連線路由傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器與現有的會話。</span><span class="sxs-lookup"><span data-stu-id="e6c15-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="e6c15-106">如果不是，則 TS 會話代理人會將連入連線以最少的會話路由傳送至 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6c15-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="e6c15-107">您可以使用 [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM 介面擴充 TS 會話代理人。</span><span class="sxs-lookup"><span data-stu-id="e6c15-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="e6c15-108">您可以使用此介面來管理 RD 工作階段主機伺服器的連線，以及任何類型的遠端桌面通訊協定 (RDP) 連線，例如在 Windows Server 2008 Hyper-v 虛擬機器主機上執行 Windows Vista Enterprise 集中化桌面 (VECD) 的來賓虛擬機器連線。</span><span class="sxs-lookup"><span data-stu-id="e6c15-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="e6c15-109">[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)介面提供幾項優點：</span><span class="sxs-lookup"><span data-stu-id="e6c15-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="e6c15-110">不需要在用戶端或 RD 工作階段主機伺服器上安裝代理程式。</span><span class="sxs-lookup"><span data-stu-id="e6c15-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="e6c15-111">外掛程式可以與其他遠端桌面服務角色服務緊密互動，例如遠端桌面閘道 (RD 閘道) ，以及依賴 TS 會話代理人有關會話和電腦狀態的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6c15-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="e6c15-112">您可以使用外掛程式來管理支援 RDP 5.2 或更新版本之用戶端或伺服器裝置的連線。</span><span class="sxs-lookup"><span data-stu-id="e6c15-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="e6c15-113">您可以使用外掛程式來啟用 Windows Vista 企業集中式桌面解決方案。</span><span class="sxs-lookup"><span data-stu-id="e6c15-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="e6c15-114">當您執行此介面的方法時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="e6c15-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="e6c15-115">TS 會話代理人可能會從多個執行緒呼叫這個 COM 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="e6c15-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="e6c15-116">如果任何呼叫的方法不會立即和成功傳回，TS 會話代理人就不會再呼叫該外掛程式並還原為其原生負載平衡邏輯。</span><span class="sxs-lookup"><span data-stu-id="e6c15-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="e6c15-117">若要繼續呼叫外掛程式，您必須重新開機終端機服務會話代理人服務。</span><span class="sxs-lookup"><span data-stu-id="e6c15-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="e6c15-118">您必須使用 Regsvr32.exe，將外掛程式註冊為整個系統的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e6c15-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="e6c15-119">因為終端機服務會話代理人服務是在 "NetworkService" 帳戶下執行，所以您必須使用 Dcomcnfg.exe 為 "NetworkService" 帳戶提供必要的啟動、啟用和存取權限。</span><span class="sxs-lookup"><span data-stu-id="e6c15-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="e6c15-120">終端機服務會話代理人服務會在下列登錄子機碼中尋找代表外掛程式的 COM 物件 CLSID：</span><span class="sxs-lookup"><span data-stu-id="e6c15-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="e6c15-121">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **參數** \\ **ExtensibilityPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="e6c15-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="e6c15-122">如需 Dcomcnfg.exe 的詳細資訊，請參閱 [使用 DCOMCNFG 啟用 COM 安全性](/windows/desktop/com/enabling-com-security-using-dcomcnfg)。</span><span class="sxs-lookup"><span data-stu-id="e6c15-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6c15-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6c15-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6c15-124">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="e6c15-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 