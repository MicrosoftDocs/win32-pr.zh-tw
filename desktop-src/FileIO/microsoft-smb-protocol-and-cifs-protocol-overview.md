---
description: 描述 Microsoft 如何將 Server Message Block (SMB) 通訊協定的執行。
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Microsoft SMB 通訊協定和 CIFS 通訊協定總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943387"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a><span data-ttu-id="9133e-103">Microsoft SMB 通訊協定和 CIFS 通訊協定總覽</span><span class="sxs-lookup"><span data-stu-id="9133e-103">Microsoft SMB Protocol and CIFS Protocol Overview</span></span>

<span data-ttu-id="9133e-104">伺服器訊息區 (SMB) 通訊協定是一個網路檔案共用通訊協定，在 Microsoft Windows 中實作為實作為 Microsoft SMB 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9133e-104">The Server Message Block (SMB) Protocol is a network file sharing protocol, and as implemented in Microsoft Windows is known as Microsoft SMB Protocol.</span></span> <span data-ttu-id="9133e-105">定義特定通訊協定版本的訊息封包集會稱為方言。</span><span class="sxs-lookup"><span data-stu-id="9133e-105">The set of message packets that defines a particular version of the protocol is called a dialect.</span></span> <span data-ttu-id="9133e-106">Common Internet File System (CIFS) Protocol 是 SMB 的用語。</span><span class="sxs-lookup"><span data-stu-id="9133e-106">The Common Internet File System (CIFS) Protocol is a dialect of SMB.</span></span> <span data-ttu-id="9133e-107">SMB 和 CIFS 也可在 VM、數個 Unix 版本和其他作業系統上使用。</span><span class="sxs-lookup"><span data-stu-id="9133e-107">Both SMB and CIFS are also available on VMS, several versions of Unix, and other operating systems.</span></span>

<span data-ttu-id="9133e-108">您可以從 [Common Internet File System (cifs) 檔案存取通訊協定](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b)的 MICROSOFT CORPORATION 取得 CIFS 的技術參考。</span><span class="sxs-lookup"><span data-stu-id="9133e-108">The technical reference to CIFS is available from Microsoft Corporation at [Common Internet File System (CIFS) File Access Protocol](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).</span></span>

<span data-ttu-id="9133e-109">雖然它的主要目的是檔案共用，但其他 Microsoft SMB 通訊協定功能包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="9133e-109">Although its main purpose is file sharing, additional Microsoft SMB Protocol functionality includes the following:</span></span>

-   [<span data-ttu-id="9133e-110">方言協商</span><span class="sxs-lookup"><span data-stu-id="9133e-110">Dialect negotiation</span></span>](microsoft-smb-protocol-dialects.md)
-   <span data-ttu-id="9133e-111">判斷網路上或網路流覽的其他 Microsoft SMB 通訊協定伺服器</span><span class="sxs-lookup"><span data-stu-id="9133e-111">Determining other Microsoft SMB Protocol servers on the network, or network browsing</span></span>
-   <span data-ttu-id="9133e-112">透過網路列印</span><span class="sxs-lookup"><span data-stu-id="9133e-112">Printing over a network</span></span>
-   [<span data-ttu-id="9133e-113">檔案、目錄和共用存取驗證</span><span class="sxs-lookup"><span data-stu-id="9133e-113">File, directory, and share access authentication</span></span>](microsoft-smb-protocol-authentication.md)
-   <span data-ttu-id="9133e-114">檔案和記錄鎖定</span><span class="sxs-lookup"><span data-stu-id="9133e-114">File and record locking</span></span>
-   <span data-ttu-id="9133e-115">檔案和目錄變更通知</span><span class="sxs-lookup"><span data-stu-id="9133e-115">File and directory change notification</span></span>
-   <span data-ttu-id="9133e-116">擴充檔案屬性處理</span><span class="sxs-lookup"><span data-stu-id="9133e-116">Extended file attribute handling</span></span>
-   <span data-ttu-id="9133e-117">Unicode 支援</span><span class="sxs-lookup"><span data-stu-id="9133e-117">Unicode support</span></span>
-   [<span data-ttu-id="9133e-118">隨機鎖定</span><span class="sxs-lookup"><span data-stu-id="9133e-118">Opportunistic locks</span></span>](opportunistic-locks.md)

<span data-ttu-id="9133e-119">在 OSI 網路模型中，Microsoft SMB 通訊協定最常用於應用層或展示層通訊協定，而且依賴較低層級的通訊協定來進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="9133e-119">In the OSI networking model, Microsoft SMB Protocol is most often used as an Application layer or a Presentation layer protocol, and it relies on lower-level protocols for transport.</span></span> <span data-ttu-id="9133e-120">Microsoft SMB 通訊協定最常使用的傳輸層通訊協定是 NetBIOS over TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="9133e-120">The transport layer protocol that Microsoft SMB Protocol is most often used with is NetBIOS over TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))).</span></span> <span data-ttu-id="9133e-121">不過，您也可以在不使用個別傳輸通訊協定的情況下使用 Microsoft SMB 通訊協定。 Microsoft SMB 通訊協定/NBT 組合通常用於回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="9133e-121">However, Microsoft SMB Protocol can also be used without a separate transport protocol the Microsoft SMB Protocol/NBT combination is generally used for backward compatibility.</span></span>

<span data-ttu-id="9133e-122">Microsoft SMB 通訊協定是一種用戶端-伺服器的執行方式，是由一組資料封包所組成，每個封包都包含用戶端傳送的要求，或由伺服器傳送的回應。</span><span class="sxs-lookup"><span data-stu-id="9133e-122">The Microsoft SMB Protocol is a client-server implementation and consists of a set of data packets, each containing a request sent by the client or a response sent by the server.</span></span> <span data-ttu-id="9133e-123">這些封包可以廣泛分類，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9133e-123">These packets can be broadly classified as follows:</span></span>

-   <span data-ttu-id="9133e-124">會話控制封包會建立並停止共用伺服器資源的連接。</span><span class="sxs-lookup"><span data-stu-id="9133e-124">Session control packets Establishes and discontinues a connection to shared server resources.</span></span>
-   <span data-ttu-id="9133e-125">檔案存取封包會存取和操作遠端伺服器上的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="9133e-125">File access packets Accesses and manipulates files and directories on the remote server.</span></span>
-   <span data-ttu-id="9133e-126">一般訊息封包會將資料傳送到列印佇列、mailslots 和具名管道，以及提供有關列印佇列狀態的資料。</span><span class="sxs-lookup"><span data-stu-id="9133e-126">General message packets Sends data to print queues, mailslots, and named pipes, and provides data about the status of print queues.</span></span>

<span data-ttu-id="9133e-127">某些訊息封包可能會在一次傳輸中分組並傳送，以降低回應延遲並增加網路頻寬。</span><span class="sxs-lookup"><span data-stu-id="9133e-127">Some message packets may be grouped and sent in one transmission to reduce response latency and increase network bandwidth.</span></span> <span data-ttu-id="9133e-128">這稱為「批次處理」。</span><span class="sxs-lookup"><span data-stu-id="9133e-128">This is called "batching."</span></span> <span data-ttu-id="9133e-129">[MICROSOFT Smb 通訊協定封包交換案例](microsoft-smb-protocol-packet-exchange-scenario.md)一節說明使用封包批次處理的 Microsoft Smb 通訊協定會話範例。</span><span class="sxs-lookup"><span data-stu-id="9133e-129">The [Microsoft SMB Protocol Packet Exchange Scenario](microsoft-smb-protocol-packet-exchange-scenario.md) section describes an example of a Microsoft SMB Protocol session that uses packet batching.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9133e-130">本節內容</span><span class="sxs-lookup"><span data-stu-id="9133e-130">In this section</span></span>



| <span data-ttu-id="9133e-131">主題</span><span class="sxs-lookup"><span data-stu-id="9133e-131">Topic</span></span>                                                                                                             | <span data-ttu-id="9133e-132">描述</span><span class="sxs-lookup"><span data-stu-id="9133e-132">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9133e-133">Microsoft SMB 通訊協定方言</span><span class="sxs-lookup"><span data-stu-id="9133e-133">Microsoft SMB Protocol Dialects</span></span>](microsoft-smb-protocol-dialects.md)<br/>                                 | <span data-ttu-id="9133e-134">若要使用 Microsoft SMB 通訊協定在用戶端與伺服器之間建立連線，您必須先使用用戶端和伺服器支援的最高層級功能來判斷方言。</span><span class="sxs-lookup"><span data-stu-id="9133e-134">To establish a connection between a client and a server using Microsoft SMB Protocol, you must first determine the dialect with the highest level of functionality that both the client and server support.</span></span><br/>                                                      |
| [<span data-ttu-id="9133e-135">Microsoft SMB 通訊協定驗證</span><span class="sxs-lookup"><span data-stu-id="9133e-135">Microsoft SMB Protocol Authentication</span></span>](microsoft-smb-protocol-authentication.md)<br/>                     | <span data-ttu-id="9133e-136">Microsoft SMB 通訊協定中使用的安全性模型與其他 SMB 變數所使用的模型相同，且包含兩個層級的安全性使用者和共用。</span><span class="sxs-lookup"><span data-stu-id="9133e-136">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security user and share.</span></span> <span data-ttu-id="9133e-137">共用是可由 Microsoft SMB 通訊協定用戶端存取的檔案、目錄或印表機。</span><span class="sxs-lookup"><span data-stu-id="9133e-137">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span><br/> |
| [<span data-ttu-id="9133e-138">Microsoft SMB 通訊協定封包交換案例</span><span class="sxs-lookup"><span data-stu-id="9133e-138">Microsoft SMB Protocol Packet Exchange Scenario</span></span>](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | <span data-ttu-id="9133e-139">用戶端與伺服器之間的 Microsoft SMB 通訊協定封包交換範例。</span><span class="sxs-lookup"><span data-stu-id="9133e-139">Example of a Microsoft SMB Protocol packet exchange between a client and a server.</span></span><br/>                                                                                                                                                                               |



 

 

