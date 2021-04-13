---
title: 使用網路原則伺服器進行記錄
description: 使用網路原則伺服器進行記錄
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315838"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="baa6e-103">使用網路原則伺服器進行記錄</span><span class="sxs-lookup"><span data-stu-id="baa6e-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="baa6e-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="baa6e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="baa6e-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="baa6e-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="baa6e-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="baa6e-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="baa6e-107">下表僅說明 RADIUS 帳戶處理封包的最重要層面。</span><span class="sxs-lookup"><span data-stu-id="baa6e-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="baa6e-108">註釋檔的 RADIUS 帳戶處理要求 ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) 提供這些封包的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="baa6e-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="baa6e-109">RADIUS 帳戶處理封包可以分為下列類別。</span><span class="sxs-lookup"><span data-stu-id="baa6e-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="baa6e-110">帳戶處理封包</span><span class="sxs-lookup"><span data-stu-id="baa6e-110">Accounting packet</span></span>  | <span data-ttu-id="baa6e-111">Description</span><span class="sxs-lookup"><span data-stu-id="baa6e-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa6e-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="baa6e-112">Accounting-On</span></span>      | <span data-ttu-id="baa6e-113">由網路存取伺服器傳送 (NAS) ，以指出它已重新開機。</span><span class="sxs-lookup"><span data-stu-id="baa6e-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="baa6e-114">包含 nas 識別碼/ipaddress。</span><span class="sxs-lookup"><span data-stu-id="baa6e-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="baa6e-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="baa6e-115">Accounting-Off</span></span>     | <span data-ttu-id="baa6e-116">由 NAS 傳送以表示正在關閉。</span><span class="sxs-lookup"><span data-stu-id="baa6e-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="baa6e-117">包含 nas 識別碼/ipaddress。</span><span class="sxs-lookup"><span data-stu-id="baa6e-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="baa6e-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="baa6e-118">Accounting-Start</span></span>   | <span data-ttu-id="baa6e-119">由 NAS 在使用者經過驗證和授權之後傳送，以指出使用者會話的啟動。</span><span class="sxs-lookup"><span data-stu-id="baa6e-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="baa6e-120">包含 userid、nas 識別碼/ipaddress，以及從 NAS 接收的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="baa6e-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="baa6e-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="baa6e-121">Accounting-Stop</span></span>    | <span data-ttu-id="baa6e-122">由 NAS 傳送以表示使用者會話的結束。</span><span class="sxs-lookup"><span data-stu-id="baa6e-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="baa6e-123">包含 userid、nas 識別碼/ipaddress，以及從 NAS 接收的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="baa6e-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="baa6e-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="baa6e-124">Accounting-Interim</span></span> | <span data-ttu-id="baa6e-125">可能會由 NAS 定期傳送到 NAS 上登入的每位使用者。</span><span class="sxs-lookup"><span data-stu-id="baa6e-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="baa6e-126">這項功能在較新版本的 NAS 中通常會受到支援。</span><span class="sxs-lookup"><span data-stu-id="baa6e-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="baa6e-127">收集可透過 RADIUS 取得的帳戶處理資訊時，請務必考慮下列問題：</span><span class="sxs-lookup"><span data-stu-id="baa6e-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="baa6e-128">在罕見的情況下，封包可能會在傳輸期間遺失，且可能永遠不會到達 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="baa6e-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="baa6e-129">如果 NAS 中止，RADIUS 伺服器就不會收到通知。</span><span class="sxs-lookup"><span data-stu-id="baa6e-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="baa6e-130">ISDN 支援多個會話，且每個會話都會產生一組計量啟動/停止封包。</span><span class="sxs-lookup"><span data-stu-id="baa6e-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="baa6e-131">有一個會計屬性稱為多會話識別碼，可清楚識別這類多會話封包。</span><span class="sxs-lookup"><span data-stu-id="baa6e-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="baa6e-132">除了會話識別碼之外，請檢查多會話識別碼，以計算會話的數目。</span><span class="sxs-lookup"><span data-stu-id="baa6e-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="baa6e-133">NPS 所記錄的要求</span><span class="sxs-lookup"><span data-stu-id="baa6e-133">Requests Logged by NPS</span></span>

<span data-ttu-id="baa6e-134">NPS 預設不會記錄任何資料。</span><span class="sxs-lookup"><span data-stu-id="baa6e-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="baa6e-135">NPS 可以使用 nps 使用者介面 (node.js) 來進行設定，以記錄下列要求。</span><span class="sxs-lookup"><span data-stu-id="baa6e-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="baa6e-136">記錄的封包</span><span class="sxs-lookup"><span data-stu-id="baa6e-136">Logged packet</span></span>          | <span data-ttu-id="baa6e-137">Description</span><span class="sxs-lookup"><span data-stu-id="baa6e-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa6e-138">帳戶處理要求</span><span class="sxs-lookup"><span data-stu-id="baa6e-138">Accounting Request</span></span>     | <span data-ttu-id="baa6e-139">上表中所述的任何會計封包。</span><span class="sxs-lookup"><span data-stu-id="baa6e-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="baa6e-140">驗證要求</span><span class="sxs-lookup"><span data-stu-id="baa6e-140">Authentication Request</span></span> | <span data-ttu-id="baa6e-141">由 NAS 代表連接的使用者傳送。</span><span class="sxs-lookup"><span data-stu-id="baa6e-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="baa6e-142">記錄專案只包含傳入屬性。</span><span class="sxs-lookup"><span data-stu-id="baa6e-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="baa6e-143">驗證接受</span><span class="sxs-lookup"><span data-stu-id="baa6e-143">Authentication Accept</span></span>  | <span data-ttu-id="baa6e-144">由 NPS 傳送以表示應接受使用者連接。</span><span class="sxs-lookup"><span data-stu-id="baa6e-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="baa6e-145">記錄專案只包含傳出屬性。</span><span class="sxs-lookup"><span data-stu-id="baa6e-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="baa6e-146">驗證拒絕</span><span class="sxs-lookup"><span data-stu-id="baa6e-146">Authentication Reject</span></span>  | <span data-ttu-id="baa6e-147">由 NPS 傳送，以指出應該拒絕使用者連接。</span><span class="sxs-lookup"><span data-stu-id="baa6e-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="baa6e-148">記錄專案只包含傳出屬性。</span><span class="sxs-lookup"><span data-stu-id="baa6e-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="baa6e-149">NPS 所記錄的資料可以移至 NPS 伺服器上的文字檔，或移至中央 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="baa6e-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="baa6e-150">如需 NPS SQL 記錄的詳細資訊，請參閱 [sql](sql-programmability.md)程式設計。</span><span class="sxs-lookup"><span data-stu-id="baa6e-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="baa6e-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="baa6e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa6e-152">網際網路驗證服務和網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="baa6e-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="baa6e-153">RADIUS 驗證、授權和帳戶處理</span><span class="sxs-lookup"><span data-stu-id="baa6e-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="baa6e-154">使用狀態伺服器</span><span class="sxs-lookup"><span data-stu-id="baa6e-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

