---
title: RAS 連接作業
description: Windows NT 和更新版本會提供 RasPhonebookDlg 和 RasDialDlg 函式，以顯示用來啟動 RAS 連接作業的內建使用者介面。
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- 連接作業，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e2a78d34afd5aea3670730656e97886b6a5916
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842508"
---
# <a name="ras-connection-operations"></a><span data-ttu-id="09a6a-104">RAS 連接作業</span><span class="sxs-lookup"><span data-stu-id="09a6a-104">RAS Connection Operations</span></span>

<span data-ttu-id="09a6a-105">Windows NT 和更新版本會提供 [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) 和 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) 函式，以顯示用來啟動 RAS 連接作業的內建使用者介面。</span><span class="sxs-lookup"><span data-stu-id="09a6a-105">Windows NT and later versions provide the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) functions that display the built-in user interface for starting a RAS connection operation.</span></span> <span data-ttu-id="09a6a-106">對於大部分的應用程式而言，這是啟動 RAS 連線作業的慣用方式。</span><span class="sxs-lookup"><span data-stu-id="09a6a-106">For most applications, this is the preferred way to start a RAS connection operation.</span></span> <span data-ttu-id="09a6a-107">Windows 95 目前不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="09a6a-107">Windows 95 does not currently support these functions.</span></span>

<span data-ttu-id="09a6a-108">本節的其餘部分將說明啟動 RAS 連接的低層級功能。</span><span class="sxs-lookup"><span data-stu-id="09a6a-108">The remainder of this section describes the low-level functions for starting a RAS connection.</span></span> <span data-ttu-id="09a6a-109">這些功能可在 bothWindows NT 4.0 (和更新版本) 和 Windows 95 上取得。</span><span class="sxs-lookup"><span data-stu-id="09a6a-109">These functions are available on bothWindows NT 4.0 (and later versions), and Windows 95.</span></span>

<span data-ttu-id="09a6a-110">RAS 用戶端應用程式會使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 功能來建立與 RAS 伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="09a6a-110">A RAS client application uses the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to establish a connection to a RAS server.</span></span> <span data-ttu-id="09a6a-111">**RasDial** 函式會啟動連接作業，然後遠端存取連線管理員會執行此作業。</span><span class="sxs-lookup"><span data-stu-id="09a6a-111">The **RasDial** function starts the connection operation, which is then carried out by the Remote Access Connection Manager.</span></span>

<span data-ttu-id="09a6a-112">遠端存取連線管理員是一項服務，可處理建立遠端伺服器連線的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="09a6a-112">The Remote Access Connection Manager is a service that handles the details of establishing the connection to the remote server.</span></span> <span data-ttu-id="09a6a-113">此服務也會在連接作業期間提供用戶端狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="09a6a-113">This service also provides the client with status information during the connection operation.</span></span> <span data-ttu-id="09a6a-114">當應用程式載入 RASAPI32.DLL 時，會自動啟動遠端存取連線管理員。</span><span class="sxs-lookup"><span data-stu-id="09a6a-114">The Remote Access Connection Manager starts automatically when an application loads the RASAPI32.DLL.</span></span>

<span data-ttu-id="09a6a-115">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫會在啟動連接作業時指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="09a6a-115">The [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call specifies the following information when it starts a connection operation:</span></span>

-   <span data-ttu-id="09a6a-116">遠端存取連線管理員建立連接所需的 [連接資訊](phone-book-files-and-connection-information.md) 。</span><span class="sxs-lookup"><span data-stu-id="09a6a-116">The [connection information](phone-book-files-and-connection-information.md) that the Remote Access Connection Manager needs to establish the connection.</span></span>
-   <span data-ttu-id="09a6a-117">選擇性的 [通知處理常式，此處理程式](notification-handlers.md) 會在連接操作期間接收進度通知。</span><span class="sxs-lookup"><span data-stu-id="09a6a-117">An optional [notification handler](notification-handlers.md) that receives progress notifications during the connection operation.</span></span> <span data-ttu-id="09a6a-118">如果 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫指定通知處理常式，則呼叫是 [非同步](asynchronous-operations.md)的;否則，它是 [同步](synchronous-operations.md)的。</span><span class="sxs-lookup"><span data-stu-id="09a6a-118">If the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call specifies a notification handler, the call is [asynchronous](asynchronous-operations.md); otherwise, it is [synchronous](synchronous-operations.md).</span></span>
-   <span data-ttu-id="09a6a-119">選擇性的 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) 結構，可啟用或停用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 作業的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="09a6a-119">An optional [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) structure to enable or disable extensions to the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) operation.</span></span> <span data-ttu-id="09a6a-120">擴充功能可讓 RAS 用戶端直接啟用某些數據機設定，以控制 RAS 是否使用電話簿專案中的前置詞和尾碼，以及支援連接作業期間的 [暫停狀態](paused-states.md) 。</span><span class="sxs-lookup"><span data-stu-id="09a6a-120">The extensions permit a RAS client to directly enable some modem settings, to control whether RAS uses the prefixes and suffixes in a phone-book entry, and to support [paused states](paused-states.md) during the connection operation.</span></span>

 

 