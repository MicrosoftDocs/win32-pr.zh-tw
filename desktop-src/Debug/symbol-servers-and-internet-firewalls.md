---
description: 某些系統會使用需要驗證所有網際網路流量的網際網路防火牆或 proxy 伺服器。
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: 符號伺服器和網際網路防火牆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510428"
---
# <a name="symbol-server-and-internet-firewalls"></a><span data-ttu-id="b5dc5-103">符號伺服器和網際網路防火牆</span><span class="sxs-lookup"><span data-stu-id="b5dc5-103">Symbol Server and Internet Firewalls</span></span>

<span data-ttu-id="b5dc5-104">某些系統會使用需要驗證所有網際網路流量的網際網路防火牆或 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-104">Some systems use Internet firewalls or proxy servers that require authentication for all Internet traffic.</span></span> <span data-ttu-id="b5dc5-105">除非系統使用以透明方式處理驗證的防火牆用戶端，否則符號伺服器的早期版本無法從網際網路存取符號。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-105">Early versions of the symbol server could not access symbols from the Internet unless the system used a firewall client that handled the authentication transparently.</span></span>

<span data-ttu-id="b5dc5-106">從 Dbghelp 6.1 開始，符號伺服器支援需要這類驗證的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-106">Starting with Dbghelp 6.1, the symbol server supports proxy servers that require such authentication.</span></span> <span data-ttu-id="b5dc5-107">符號伺服器會使用在電腦的 LAN 設定中設定為預設值的任何伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-107">The symbol server uses whatever server is configured as the default in the computer's LAN settings.</span></span> <span data-ttu-id="b5dc5-108">若要找到此專案，請在主控台中開啟 [ **網際網路選項** **]，** 按一下 [連線] 索引標籤，然後按一下 [ **區域網路設定**]</span><span class="sxs-lookup"><span data-stu-id="b5dc5-108">To find this, open the **Internet Options** item in Control Panel, click the **Connections** tab and click **LAN Settings**.</span></span> <span data-ttu-id="b5dc5-109">您也可以按一下 [**工具**] 功能表上的 [**網際網路選項**]，從 Internet Explorer 完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-109">This can also be done from Internet Explorer by clicking **Internet Options** on the **Tools** menu.</span></span> <span data-ttu-id="b5dc5-110">符號伺服器已使用驗證的基本和挑戰回應方法，在許多品牌的 proxy 伺服器上進行測試。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-110">The symbol server has been tested on many brands of proxy servers using both basic and challenge-response methods of authentication.</span></span>

<span data-ttu-id="b5dc5-111">若要為要使用的符號伺服器定義特定的 proxy 伺服器，請將 \_ NT \_ 符號 \_ proxy 環境變數設定為 proxy 伺服器的名稱 (或 IP 位址) ，後面接著埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-111">To define a specific proxy server for symbol server to use, set the \_NT\_SYMBOL\_PROXY environment variable to the name (or IP address) of the proxy server, followed by the port number.</span></span> <span data-ttu-id="b5dc5-112">以冒號分隔兩個值。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-112">Separate the two values with a colon.</span></span> <span data-ttu-id="b5dc5-113">例如：</span><span class="sxs-lookup"><span data-stu-id="b5dc5-113">For example:</span></span>

<span data-ttu-id="b5dc5-114">**設定 \_NT \_ 符號 \_ PROXY =**_myproxyserver_*_： 80_*</span><span class="sxs-lookup"><span data-stu-id="b5dc5-114">**set \_NT\_SYMBOL\_PROXY=**_myproxyserver_*_:80_*</span></span>

<span data-ttu-id="b5dc5-115">使用 windbg 偵錯工具時，請將符號路徑設定為指向您想要使用的符號存放區。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-115">When using the windbg debugger, configure your symbol path to point to the symbol store that you want to use.</span></span> <span data-ttu-id="b5dc5-116">其中一個差異是系統會顯示一個對話方塊，您必須在此對話方塊中輸入您的使用者識別碼和密碼，才能傳遞至 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-116">The one difference is that the system will display a dialog box in which you need to enter your user ID and password to pass to the proxy server.</span></span> <span data-ttu-id="b5dc5-117">如果您輸入不正確的資訊，將會重新顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-117">If you enter incorrect information, the dialog box will be redisplayed.</span></span> <span data-ttu-id="b5dc5-118">如果您按一下 [ **取消** ] 按鈕，則會關閉對話方塊，並停用符號伺服器以透過網際網路使用。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-118">If you click the **Cancel** button, the dialog box is dismissed and the symbol server will be disabled for use through the Internet.</span></span>

<span data-ttu-id="b5dc5-119">使用 cdb.exe 或 ntsd.exe 的最新版本時，預設會關閉此功能。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-119">When using the latest versions of cdb.exe or ntsd.exe, this functionality is turned off by default.</span></span> <span data-ttu-id="b5dc5-120">不過，您可以使用！ sym 擴充功能命令來啟用或停用此功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b5dc5-120">However you can enable or disable this functionality using the !sym extension command as follows:</span></span>

-   <span data-ttu-id="b5dc5-121">開啟提示輸入使用者識別碼和密碼： **！ sym 提示**。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-121">To turn on prompting for user ID and password: **!sym prompts**.</span></span>
-   <span data-ttu-id="b5dc5-122">關閉使用者識別碼和密碼： **！ sym 提示關閉** 的提示。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-122">To turn off prompting for user ID and password: **!sym prompts off**.</span></span>

<span data-ttu-id="b5dc5-123">如果您開啟提示，您將需要使用. 重載命令重載符號。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-123">If you turn on prompting, you will need to reload symbols with the .reload command.</span></span>

<span data-ttu-id="b5dc5-124">已擴充 DbgHelp API 來支援這些變更。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-124">The DbgHelp API has been expanded to support these changes.</span></span> <span data-ttu-id="b5dc5-125">[**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85))函數支援 SSRVOPT \_ PROXY 選項。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-125">The [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) function supports the SSRVOPT\_PROXY option.</span></span> <span data-ttu-id="b5dc5-126">如果資料參數為 **Null**，則會使用 [ **網際網路選項** ] 中定義的預設 proxy。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-126">If the data parameter is **NULL**, the default proxy defined in **Internet Options** is used.</span></span> <span data-ttu-id="b5dc5-127">否則，會傳遞以零結束的字串，指定 proxy 伺服器的名稱和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-127">Otherwise a zero-terminated string is passed specifying the name and port number of the proxy server.</span></span> <span data-ttu-id="b5dc5-128">名稱和埠會以冒號分隔，如下所示： *myproxyserver*：80。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-128">The name and port are separated by a colon as follows: *myproxyserver*:80.</span></span> <span data-ttu-id="b5dc5-129">[**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函數支援 SYMOPT \_ NO \_ 提示選項。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-129">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function supports the SYMOPT\_NO\_PROMPTS option.</span></span> <span data-ttu-id="b5dc5-130">這會關閉從符號伺服器進行驗證的所有提示。</span><span class="sxs-lookup"><span data-stu-id="b5dc5-130">This turns off all prompting for validation from the symbol server.</span></span>

 

 
