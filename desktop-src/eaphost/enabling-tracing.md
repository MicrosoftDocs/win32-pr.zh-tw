---
title: 啟用 EAPHost 追蹤
description: 可協助使用者找出 EAP 驗證程式期間發生之問題的根本原因。 調試資訊可以包含執行的 API 呼叫、執行的內部函式呼叫，以及執行的狀態轉換。
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104024368"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="1d36d-104">啟用 EAPHost 追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="1d36d-105">包含偵錯工具資訊的追蹤記錄可協助使用者找出 EAP 驗證程式期間發生之問題的根本原因。</span><span class="sxs-lookup"><span data-stu-id="1d36d-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="1d36d-106">調試資訊可以包含執行的 API 呼叫、執行的內部函式呼叫，以及執行的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="1d36d-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="1d36d-107">用戶端和驗證端都可以同時啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="1d36d-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="1d36d-108">也可以對 [路由及遠端存取服務 (RRAS) ](/windows/desktop/RRAS/routing-start-page) api 的呼叫啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="1d36d-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="1d36d-109">如需詳細資訊，請參閱「 [路由及遠端存取」服務的追蹤](#tracing-on-the-routing-and-remote-access-service)。</span><span class="sxs-lookup"><span data-stu-id="1d36d-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="1d36d-110">追蹤記錄檔僅提供英文版。</span><span class="sxs-lookup"><span data-stu-id="1d36d-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="1d36d-111">啟用 EAPHost 追蹤時，記錄資訊會儲存在使用者指定位置的 .etl 檔案中。</span><span class="sxs-lookup"><span data-stu-id="1d36d-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="1d36d-112">如果在 EAP 驗證期間發生錯誤，追蹤會產生可傳送給 Microsoft 開發人員根本原因分析支援的 .etl 檔案。</span><span class="sxs-lookup"><span data-stu-id="1d36d-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="1d36d-113">具有 Microsoft windows build 共用、符號和 traceformat 檔案存取權的合作夥伴，可以使用 **tracerpt** 工具將 .etl 檔案轉換成純文字檔案。</span><span class="sxs-lookup"><span data-stu-id="1d36d-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="1d36d-114">EAPHost 記錄中不會捕捉網路原則伺服器 (NPS) 失敗。</span><span class="sxs-lookup"><span data-stu-id="1d36d-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="1d36d-115">如果您嘗試針對 NPS 失敗進行疑難排解，請參閱 IASSAM。記錄檔和 [IASNAP。記錄](https://go.microsoft.com/fwlink/p/?linkid=84108) 檔。</span><span class="sxs-lookup"><span data-stu-id="1d36d-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="1d36d-116">用戶端上的追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-116">Tracing on the Client</span></span>

<span data-ttu-id="1d36d-117">若要在用戶端上啟用追蹤：</span><span class="sxs-lookup"><span data-stu-id="1d36d-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="1d36d-118">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="1d36d-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="1d36d-119">執行下列命令： **logman** **start trace** **EapHostPeer** **-o** **。 \\EapHostPeer .etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span><span class="sxs-lookup"><span data-stu-id="1d36d-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="1d36d-120">重現您要追蹤的情節。</span><span class="sxs-lookup"><span data-stu-id="1d36d-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="1d36d-121">執行下列命令： **logman** **stop** **EapHostPeer** **-ets**</span><span class="sxs-lookup"><span data-stu-id="1d36d-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="1d36d-122">使用下列命令將 etl 檔案轉換成文字： **tracerpt EapHostPeer .etl** **– pdb** **&lt; &gt; pdbpath** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="1d36d-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="1d36d-123">如果您沒有 tracerpt 工具的存取權，請避免最後一個步驟，並將 .etl 檔案傳送給 Microsoft 開發人員支援服務。</span><span class="sxs-lookup"><span data-stu-id="1d36d-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="1d36d-124">驗證器上的追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="1d36d-125">若要啟用驗證器端的追蹤：</span><span class="sxs-lookup"><span data-stu-id="1d36d-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="1d36d-126">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="1d36d-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="1d36d-127">執行下列命令： **logman** **start trace** **EapHostAuthr** **-o** **。 \\EapHostAuthr .etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span><span class="sxs-lookup"><span data-stu-id="1d36d-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="1d36d-128">重現您要追蹤的情節。</span><span class="sxs-lookup"><span data-stu-id="1d36d-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="1d36d-129">執行下列命令： **logman** **stop** **EapHostAuthr** **-ets**</span><span class="sxs-lookup"><span data-stu-id="1d36d-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="1d36d-130">使用下列命令將 etl 檔案轉換成文字： **tracerpt EapHostAuthr .etl** **– pdb** **&lt; &gt; pdbpath** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="1d36d-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="1d36d-131">如果您沒有 tracerpt 工具的存取權，請避免最後一個步驟，改為將 .etl 檔案傳送給 Microsoft 開發人員支援人員。</span><span class="sxs-lookup"><span data-stu-id="1d36d-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="1d36d-132">事件追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-132">Event tracing</span></span>

<span data-ttu-id="1d36d-133">在 Windows 7 和更新版本的 Windows 中，EapHost 會在驗證器和對等上提供以事件為基礎的追蹤。</span><span class="sxs-lookup"><span data-stu-id="1d36d-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="1d36d-134">以事件為基礎的追蹤的優點是，不需要任何符號檔來查看追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="1d36d-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="1d36d-135">若要啟用事件追蹤：</span><span class="sxs-lookup"><span data-stu-id="1d36d-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="1d36d-136">開啟 **EventViewer**。</span><span class="sxs-lookup"><span data-stu-id="1d36d-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="1d36d-137">重要的 EapHost 訊息會記錄在以下：「自訂視圖 \\ 管理事件」</span><span class="sxs-lookup"><span data-stu-id="1d36d-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="1d36d-138">非重大訊息會記錄在：「應用程式和服務 \\ Microsoft \\ Windows \\ EapHost</span><span class="sxs-lookup"><span data-stu-id="1d36d-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="1d36d-139">從標題列的 [ **view** ] 功能表中選取 [**顯示分析和偵錯工具記錄** 檔]，即可在相同的路徑底下看到「分析」和「debug」類型事件訊息。</span><span class="sxs-lookup"><span data-stu-id="1d36d-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="1d36d-140">在路由及遠端存取服務上追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="1d36d-141">若要啟用 RRAS 追蹤：</span><span class="sxs-lookup"><span data-stu-id="1d36d-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="1d36d-142">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="1d36d-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="1d36d-143">執行下列命令： **netsh** **ras** **set** **tr** **\* *_ _* en**</span><span class="sxs-lookup"><span data-stu-id="1d36d-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="1d36d-144">開啟 **% systemroot% \\ 追蹤** 以查看 RAS 追蹤</span><span class="sxs-lookup"><span data-stu-id="1d36d-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="1d36d-145">若要停用 RRAS 追蹤：</span><span class="sxs-lookup"><span data-stu-id="1d36d-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="1d36d-146">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="1d36d-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="1d36d-147">執行下列命令： **netsh** **ras** **set** **tr** **\* *_ _***</span><span class="sxs-lookup"><span data-stu-id="1d36d-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="1d36d-148">如需詳細資訊，請參閱 [Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="1d36d-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d36d-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d36d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d36d-150">使用 EAPHost</span><span class="sxs-lookup"><span data-stu-id="1d36d-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="1d36d-151">路由及遠端存取服務 (RRAS)</span><span class="sxs-lookup"><span data-stu-id="1d36d-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 