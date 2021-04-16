---
title: 警示功能
description: 網路管理警示功能會通知網路服務程式和網路事件的應用程式。
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463365"
---
# <a name="alert-functions"></a><span data-ttu-id="d5511-103">警示功能</span><span class="sxs-lookup"><span data-stu-id="d5511-103">Alert Functions</span></span>

<span data-ttu-id="d5511-104">\[Windows Vista 不支援警示功能，因為不支援警報器和 messenger 服務。\]</span><span class="sxs-lookup"><span data-stu-id="d5511-104">\[The alert functions are not supported as of Windows Vista because the alerter and messenger services are not supported.\]</span></span>

<span data-ttu-id="d5511-105">網路管理警示功能會通知網路服務程式和網路事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5511-105">The network management alert functions notify network service programs and applications of network events.</span></span> <span data-ttu-id="d5511-106">*事件* 是由應用程式所定義的進程、出現或硬體狀態的特定實例。</span><span class="sxs-lookup"><span data-stu-id="d5511-106">An *event* is a particular instance of a process, occurrence, or state of hardware as defined by an application.</span></span> <span data-ttu-id="d5511-107">警示函數可讓應用程式指出預先定義的事件發生的時間。</span><span class="sxs-lookup"><span data-stu-id="d5511-107">The alert functions allow applications to indicate when predefined events occur.</span></span>

<span data-ttu-id="d5511-108">**Windows Server 2003：** Windows Server 2003 上預設會停用警報器和 messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="d5511-108">**Windows Server 2003:** The alerter and messenger services are disabled by default on Windows Server 2003.</span></span> <span data-ttu-id="d5511-109">您必須重新啟用服務，才能呼叫網路管理警示功能或網路管理 [訊息功能](message-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="d5511-109">You must re-enable the services before calling the network management Alert functions or the network management [Message functions](message-functions.md).</span></span>

<span data-ttu-id="d5511-110">警示功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="d5511-110">The alert functions are listed following.</span></span>



| <span data-ttu-id="d5511-111">函式</span><span class="sxs-lookup"><span data-stu-id="d5511-111">Function</span></span>                                   | <span data-ttu-id="d5511-112">描述</span><span class="sxs-lookup"><span data-stu-id="d5511-112">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5511-113">**NetAlertRaise**</span><span class="sxs-lookup"><span data-stu-id="d5511-113">**NetAlertRaise**</span></span>](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | <span data-ttu-id="d5511-114">通知所有已註冊的用戶端發生特定事件。</span><span class="sxs-lookup"><span data-stu-id="d5511-114">Notifies all registered clients that a particular event has occurred.</span></span>                                                                                                                                  |
| [<span data-ttu-id="d5511-115">**NetAlertRaiseEx**</span><span class="sxs-lookup"><span data-stu-id="d5511-115">**NetAlertRaiseEx**</span></span>](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | <span data-ttu-id="d5511-116">簡化通知已註冊的用戶端發生特定事件，因為不同于 **NetAlertRaise**， **NetAlertRaiseEx** 不需要 [**STD \_ 警示**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) 結構。</span><span class="sxs-lookup"><span data-stu-id="d5511-116">Simplifies notifying registered clients that a particular event has occurred, because, unlike **NetAlertRaise**, **NetAlertRaiseEx** does not require a [**STD\_ALERT**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) structure.</span></span> |



 

<span data-ttu-id="d5511-117">當您呼叫 **NetAlertRaise** 函數或 **NetAlertRaiseEx** 函式時，必須在用戶端電腦上執行警報器服務。</span><span class="sxs-lookup"><span data-stu-id="d5511-117">The alerter service must be running on the client computer when you call the **NetAlertRaise** function or the **NetAlertRaiseEx** function.</span></span> <span data-ttu-id="d5511-118">如果服務未執行，則函式會失敗並 **\_ \_ \_ 找不到錯誤** 檔案。</span><span class="sxs-lookup"><span data-stu-id="d5511-118">If the service is not running, the functions fail with **ERROR\_FILE\_NOT\_FOUND**.</span></span> <span data-ttu-id="d5511-119">用戶端上的警報器服務會呼叫 [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) 函數，以將資訊傳送給收件者。</span><span class="sxs-lookup"><span data-stu-id="d5511-119">The alerter service on the client calls the [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) function to send information to recipients.</span></span>

<span data-ttu-id="d5511-120">應用程式、網路服務和內部網路元件會使用網路管理警示功能來引發警示，並在發生特定類型的事件時通知各種應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="d5511-120">Applications, network services, and internal network components use the network management alert functions to raise an alert, notifying various applications or users when a particular type of event occurs.</span></span> <span data-ttu-id="d5511-121">警示類別目錄函數、資料類型、結構和常數都定義于 LMCONS 中。H、LMERR。H 和 LMALERT。H 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="d5511-121">The alert category functions, data types, structures, and constants are defined in the LMCONS.H, LMERR.H, and LMALERT.H header files.</span></span> <span data-ttu-id="d5511-122">若要存取這些定義，請定義 \_ 包含 NETERRORS 和 include NETALERT 的常數， \_ 並包含標頭檔的 LM. H。</span><span class="sxs-lookup"><span data-stu-id="d5511-122">To access these definitions, define the constants INCL\_NETERRORS and INCL\_NETALERT, and include the header file LM.H.</span></span>

<span data-ttu-id="d5511-123">LMALERT。H file 預先定義下列警示類別 () 傳送警示的網路事件種類：</span><span class="sxs-lookup"><span data-stu-id="d5511-123">The LMALERT.H file predefines the following alert classes (types of network events) for sending alerts:</span></span>

-   <span data-ttu-id="d5511-124">需要系統管理協助的網路事件</span><span class="sxs-lookup"><span data-stu-id="d5511-124">Network events requiring administrative assistance</span></span>
-   <span data-ttu-id="d5511-125">將專案新增至錯誤記錄檔</span><span class="sxs-lookup"><span data-stu-id="d5511-125">Addition of an entry to an error log file</span></span>
-   <span data-ttu-id="d5511-126">由使用者或應用程式接收廣播訊息</span><span class="sxs-lookup"><span data-stu-id="d5511-126">Reception of a broadcast message by a user or an application</span></span>
-   <span data-ttu-id="d5511-127">完成列印工作</span><span class="sxs-lookup"><span data-stu-id="d5511-127">Completion of a print job</span></span>
-   <span data-ttu-id="d5511-128">使用者使用特定應用程式或資源</span><span class="sxs-lookup"><span data-stu-id="d5511-128">Use of certain applications or resources by users</span></span>

<span data-ttu-id="d5511-129">您可以視需要定義網路應用程式的其他警示類別。</span><span class="sxs-lookup"><span data-stu-id="d5511-129">You can define other classes of alerts for network applications as needed.</span></span> <span data-ttu-id="d5511-130">例如，如果伺服器上的應用程式會定期將大量資料寫入磁片磁碟機，應用程式就會執行填滿磁片的風險。</span><span class="sxs-lookup"><span data-stu-id="d5511-130">For example, if an application on a server routinely writes large amounts of data to a disk drive, the application runs the risk of filling the disk.</span></span> <span data-ttu-id="d5511-131">在此情況下，您可能會想要新增事件「沒有可用磁碟空間」來觸發警示，通知應用程式暫停或終止正在填滿磁片的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d5511-131">In this case, you might want to add the event "no free disk space' to trigger an alert that notifies the application to pause or to terminate the process that is filling the disk.</span></span> <span data-ttu-id="d5511-132">警示的事件名稱可以是任何文字字串。</span><span class="sxs-lookup"><span data-stu-id="d5511-132">The event name for an alert can be any text string.</span></span>

<span data-ttu-id="d5511-133">當您在呼叫 [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) 函式時引發警示時，訊息資料應該包含一個 [**標準 \_ 警示**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) 標頭結構，後面接著另一個系統 [**管理員 \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info)中警示特定的固定長度資料， [**Cbenginecurr.errlog \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info)、 [**列印 \_ 其他 \_**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)資訊或 [**使用者 \_ 其他 \_ 資訊**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="d5511-133">When you raise an alert with a call to the [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) function, the message data should consist of one [**STD\_ALERT**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) header structure, followed by additional fixed-length data that is alert-specific in one [**ADMIN\_OTHER\_INFO**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info), [**ERRLOG\_OTHER\_INFO**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info), [**PRINT\_OTHER\_INFO**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info), or [**USER\_OTHER\_INFO**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) structure.</span></span> <span data-ttu-id="d5511-134">其他可變長度的資料可以遵循警示特定結構。</span><span class="sxs-lookup"><span data-stu-id="d5511-134">Additional variable-length data can follow the alert-specific structure.</span></span> <span data-ttu-id="d5511-135">[**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex)函數的 (呼叫不需要 **STD \_ 警示** 結構。 ) 呼叫端應用程式必須配置所有結構和可變長度資料的記憶體，並且在呼叫傳回之後釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="d5511-135">(Calls to the [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) function do not require a **STD\_ALERT** structure.) The calling application must allocate the memory for all structures and variable-length data, and free the memory after the call returns.</span></span>

<span data-ttu-id="d5511-136">下列宏可用於警示資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d5511-136">The following macros are available for use with alert data buffers.</span></span>



| <span data-ttu-id="d5511-137">巨集</span><span class="sxs-lookup"><span data-stu-id="d5511-137">Macro</span></span>                                          | <span data-ttu-id="d5511-138">Description</span><span class="sxs-lookup"><span data-stu-id="d5511-138">Description</span></span>                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5511-139">**警示 \_ 其他 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d5511-139">**ALERT\_OTHER\_INFO**</span></span>](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | <span data-ttu-id="d5511-140">傳回在警示訊息中遵循 **STD \_ 警示** 結構的固定長度資料指標。</span><span class="sxs-lookup"><span data-stu-id="d5511-140">Returns a pointer to the fixed-length data that follows the **STD\_ALERT** structure in an alert message.</span></span> |
| [<span data-ttu-id="d5511-141">**警示 \_ VAR \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="d5511-141">**ALERT\_VAR\_DATA**</span></span>](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | <span data-ttu-id="d5511-142">傳回變數長度資料的指標，此資料會遵循警示訊息中的警示特定資料。</span><span class="sxs-lookup"><span data-stu-id="d5511-142">Returns a pointer to the variable-length data that follows the alert-specific data in an alert message.</span></span>   |



 

<span data-ttu-id="d5511-143">您可以使用 Windows Management Instrumentation (WMI) SDK 進行事件通知，而不是使用網路管理警示功能。</span><span class="sxs-lookup"><span data-stu-id="d5511-143">Instead of using the network management alert functions, you may be able to use the Windows Management Instrumentation (WMI) SDK for event notification.</span></span> <span data-ttu-id="d5511-144">如需有關支援 WMI 事件模型之平臺的詳細資訊，請參閱 wmi 檔中的 [Wmi 基礎結構](/windows/desktop/WmiSdk/wmi-infrastructure) 和 [監視事件](/windows/desktop/WmiSdk/monitoring-events) 。</span><span class="sxs-lookup"><span data-stu-id="d5511-144">For more information about the platforms that support the WMI event model, see [WMI Infrastructure](/windows/desktop/WmiSdk/wmi-infrastructure) and [Monitoring Events](/windows/desktop/WmiSdk/monitoring-events) in the WMI documentation.</span></span>

 

 