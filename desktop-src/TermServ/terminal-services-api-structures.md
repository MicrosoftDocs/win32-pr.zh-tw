---
title: 遠端桌面服務 API 結構
description: 列出與遠端桌面服務 API 搭配使用的結構。
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092756"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="42380-103">遠端桌面服務 API 結構</span><span class="sxs-lookup"><span data-stu-id="42380-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="42380-104">下列結構會與遠端桌面服務 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="42380-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="42380-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="42380-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="42380-106">**通道 \_ 定義**</span><span class="sxs-lookup"><span data-stu-id="42380-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="42380-107">包含遠端桌面服務虛擬通道的名稱和選項。</span><span class="sxs-lookup"><span data-stu-id="42380-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-108">**通道 \_ 進入 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="42380-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="42380-109">包含用戶端 DLL 呼叫之函式的指標，以存取虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="42380-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-110">**通道 \_ PDU \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="42380-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="42380-111">包含由虛擬通道的伺服器端所接收之資料區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-112">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="42380-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="42380-113">包含特定遠端桌面服務授權金鑰套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-114">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="42380-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="42380-115">包含特定遠端桌面服務授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-116">**WTSCLIENT**</span><span class="sxs-lookup"><span data-stu-id="42380-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="42380-117">包含遠端桌面連線 (RDC) 用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-118">**WTSCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="42380-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="42380-119">包含遠端桌面服務會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-120">**WTSINFO**</span><span class="sxs-lookup"><span data-stu-id="42380-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="42380-121">包含遠端桌面服務會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-122">**WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="42380-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="42380-123">包含 [**WTSINFOEX \_ 層級**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) 聯集，其中包含遠端桌面服務會話的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-124">**WTSINFOEX \_ 級1**</span><span class="sxs-lookup"><span data-stu-id="42380-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="42380-125">包含遠端桌面服務會話的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-126">**WTSLISTENERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="42380-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="42380-127">包含遠端桌面服務接聽程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-128">**WTSSBX \_ IP \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="42380-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="42380-129">包含網路資源 IP 位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-130">**WTSSBX \_ 電腦 \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="42380-131">包含正在接受遠端連線之電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-132">**WTSSBX \_ 機器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="42380-133">包含電腦及其目前狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-134">**WTSSBX \_ 會話 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="42380-135">包含遠端桌面連線代理人 (RD 連線代理人) 可用之會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="42380-136">**WTSSESSION \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="42380-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="42380-137">提供會話變更通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-137">Provides information about the session change notification.</span></span> <span data-ttu-id="42380-138">服務會在其 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) 函式中接收此結構，以回應會話變更事件。</span><span class="sxs-lookup"><span data-stu-id="42380-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-139">**WTSUSERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="42380-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="42380-140">包含網域控制站或遠端桌面工作階段主機 (RD 工作階段主機) server 上使用者的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-141">**WTS \_ 用戶端 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="42380-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="42380-142">包含遠端桌面服務會話的用戶端網路位址。</span><span class="sxs-lookup"><span data-stu-id="42380-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-143">**WTS \_ 用戶端 \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="42380-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="42380-144">包含遠端桌面連線 (RDC) 用戶端顯示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-145">**WTS \_ 流程 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="42380-146">包含在 RD 工作階段主機伺服器上執行之進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-147">**WTS \_ 進程 \_ 資訊， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="42380-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="42380-148">包含在 RD 工作階段主機伺服器上執行之進程的擴充資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="42380-149">[**WTS \_ 產品 \_ 資訊**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="42380-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="42380-150">連接到終端機伺服器所需的產品授權詳細資料。</span><span class="sxs-lookup"><span data-stu-id="42380-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-151">**WTS \_ 伺服器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="42380-152">包含特定遠端桌面服務伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-153">**WTS \_ 會話 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="42380-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="42380-154">包含指派給會話的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="42380-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-155">**WTS \_ 會話 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42380-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="42380-156">包含 RD 工作階段主機伺服器上用戶端會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="42380-157">**WTS \_ 會話 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="42380-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="42380-158">包含 RD 工作階段主機伺服器或遠端桌面虛擬化主機 (RD 虛擬化主機) 伺服器上用戶端會話的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="42380-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 