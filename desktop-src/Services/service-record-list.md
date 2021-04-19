---
description: 由於每個服務專案都是從已安裝服務的資料庫讀取，因此 SCM 會建立服務的服務記錄。
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: 服務記錄清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1143625de977c7e5c488c5cc56620adc3a5454db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997086"
---
# <a name="service-record-list"></a><span data-ttu-id="4d767-103">服務記錄清單</span><span class="sxs-lookup"><span data-stu-id="4d767-103">Service Record List</span></span>

<span data-ttu-id="4d767-104">由於每個服務專案都是從已安裝服務的資料庫讀取，因此 SCM 會建立服務的服務記錄。</span><span class="sxs-lookup"><span data-stu-id="4d767-104">As each service entry is read from the database of installed services, the SCM creates a service record for the service.</span></span> <span data-ttu-id="4d767-105">服務記錄包含：</span><span class="sxs-lookup"><span data-stu-id="4d767-105">A service record includes:</span></span>

-   <span data-ttu-id="4d767-106">服務名稱</span><span class="sxs-lookup"><span data-stu-id="4d767-106">Service name</span></span>
-   <span data-ttu-id="4d767-107">啟動類型 (自動啟動或需求-開始) </span><span class="sxs-lookup"><span data-stu-id="4d767-107">Start type (auto-start or demand-start)</span></span>
-   <span data-ttu-id="4d767-108">服務狀態 (查看 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) 結構) </span><span class="sxs-lookup"><span data-stu-id="4d767-108">Service status (see the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure)</span></span> <dl> <span data-ttu-id="4d767-109">類型</span><span class="sxs-lookup"><span data-stu-id="4d767-109">Type</span></span>  
    <span data-ttu-id="4d767-110">目前狀態</span><span class="sxs-lookup"><span data-stu-id="4d767-110">Current state</span></span>  
    <span data-ttu-id="4d767-111">可接受的控制碼</span><span class="sxs-lookup"><span data-stu-id="4d767-111">Acceptable control codes</span></span>  
    <span data-ttu-id="4d767-112">結束碼</span><span class="sxs-lookup"><span data-stu-id="4d767-112">Exit code</span></span>  
    <span data-ttu-id="4d767-113">Wait 提示</span><span class="sxs-lookup"><span data-stu-id="4d767-113">Wait hint</span></span>  
    </dl>
-   Pointer to dependency list

<span data-ttu-id="4d767-114">安裝服務時，會指定帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-114">The user name and password of an account are specified at the time the service is installed.</span></span> <span data-ttu-id="4d767-115">SCM 會將使用者名稱儲存在登錄中，並將密碼儲存在本機安全機構 (LSA) 的安全部分。</span><span class="sxs-lookup"><span data-stu-id="4d767-115">The SCM stores the user name in the registry and the password in a secure portion of the Local Security Authority (LSA).</span></span> <span data-ttu-id="4d767-116">系統管理員可以建立密碼永遠不會過期的帳戶。</span><span class="sxs-lookup"><span data-stu-id="4d767-116">The system administrator can create accounts with passwords that never expire.</span></span> <span data-ttu-id="4d767-117">或者，系統管理員可以建立具有密碼的帳戶，藉由定期變更密碼來過期及管理帳戶。</span><span class="sxs-lookup"><span data-stu-id="4d767-117">Alternatively, the system administrator can create accounts with passwords that expire and manage the accounts by changing the passwords periodically.</span></span>

<span data-ttu-id="4d767-118">SCM 會保留使用者帳戶密碼的兩個複本，也就是目前的密碼和備份密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-118">The SCM keeps two copies of a user account's password, a current password and a backup password.</span></span> <span data-ttu-id="4d767-119">第一次安裝服務時指定的密碼會儲存為目前的密碼，且不會初始化備份密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-119">The password specified the first time the service is installed is stored as the current password and the backup password is not initialized.</span></span> <span data-ttu-id="4d767-120">當 SCM 嘗試在使用者帳戶的安全性內容中執行服務時，會使用目前的密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-120">When the SCM attempts to run the service in the security context of the user account, it uses the current password.</span></span> <span data-ttu-id="4d767-121">如果成功使用目前的密碼，也會另存為備份密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-121">If the current password is used successfully, it is also saved as the backup password.</span></span> <span data-ttu-id="4d767-122">如果使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 函式或 [服務] 控制台公用程式來修改密碼，則新密碼會儲存為目前的密碼，而先前的密碼會儲存為備份密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-122">If the password is modified with the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function, or the Services control panel utility, the new password is stored as the current password and the previous password is stored as the backup password.</span></span> <span data-ttu-id="4d767-123">如果 SCM 嘗試啟動服務，但目前的密碼失敗，則會使用備份密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-123">If the SCM attempts to start the service and the current password fails, then it uses the backup password.</span></span> <span data-ttu-id="4d767-124">如果成功使用備份密碼，則會儲存為目前的密碼。</span><span class="sxs-lookup"><span data-stu-id="4d767-124">If the backup password is used successfully, it is saved as the current password.</span></span>

<span data-ttu-id="4d767-125">當服務使用 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函數傳送狀態通知時，SCM 會更新服務狀態。</span><span class="sxs-lookup"><span data-stu-id="4d767-125">The SCM updates the service status when a service sends it status notifications using the [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) function.</span></span> <span data-ttu-id="4d767-126">SCM 會藉由查詢 i/o 系統來維護驅動程式服務的狀態，而不是從服務收到狀態通知。</span><span class="sxs-lookup"><span data-stu-id="4d767-126">The SCM maintains the status of a driver service by querying the I/O system, instead of receiving status notifications, as it does from a service.</span></span>

<span data-ttu-id="4d767-127">服務可以藉由呼叫 [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) 函數來註冊其他類型資訊。</span><span class="sxs-lookup"><span data-stu-id="4d767-127">A service can register additional type information by calling the [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) function.</span></span> <span data-ttu-id="4d767-128">[**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo)和 [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum)函數會取得支援的服務類型。</span><span class="sxs-lookup"><span data-stu-id="4d767-128">The [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) and [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) functions obtain the supported service types.</span></span>

 

 
