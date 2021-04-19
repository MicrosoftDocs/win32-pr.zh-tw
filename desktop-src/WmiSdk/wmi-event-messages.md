---
description: 下列清單列出 Windows Vista 和更新版本作業系統中的 WMI 記錄檔所支援的事件。
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: WMI 事件訊息
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979083"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="e69bd-103">WMI 事件訊息</span><span class="sxs-lookup"><span data-stu-id="e69bd-103">WMI Event Messages</span></span>

<span data-ttu-id="e69bd-104">下列清單列出 Windows Vista 和更新版本作業系統中的 WMI 記錄檔所支援的事件。</span><span class="sxs-lookup"><span data-stu-id="e69bd-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="e69bd-105">下列檔是專為開發人員和 IT 系統管理員所設計。</span><span class="sxs-lookup"><span data-stu-id="e69bd-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="e69bd-106">如果您嘗試在家庭系統上解決 WMI 錯誤訊息，請參閱 [Microsoft 支援服務](https://support.microsoft.com/) 網站。</span><span class="sxs-lookup"><span data-stu-id="e69bd-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="e69bd-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ MC 存放 \_ 庫 \_ 不一致**</span><span class="sxs-lookup"><span data-stu-id="e69bd-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-108">1073747424 (0x400015E0) </span><span class="sxs-lookup"><span data-stu-id="e69bd-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-109">Windows Management Instrumentation 服務偵測到目錄 *% windir% \\ system32 \\ wbem 存放 \\ 庫* 中的 WMI 存放庫不一致，因此無法加以復原。</span><span class="sxs-lookup"><span data-stu-id="e69bd-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="e69bd-110">現在將刪除 WMI 儲存機制，系統會根據自動復原機制來建立新的存放庫。</span><span class="sxs-lookup"><span data-stu-id="e69bd-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM \_ MC \_ 提供者 \_ 子系統 \_ LOCALSYSTEM \_ 提供者 \_ 載入**</span><span class="sxs-lookup"><span data-stu-id="e69bd-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-112">2147483711 (0x8000003F) </span><span class="sxs-lookup"><span data-stu-id="e69bd-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-113">已在 Windows Management Instrumentation 命名空間 %2 中註冊提供者 %1，以使用 LocalSystem 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e69bd-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="e69bd-114">此帳戶具有特殊許可權，如果提供者未正確地模擬使用者要求，則可能會造成安全性違規。</span><span class="sxs-lookup"><span data-stu-id="e69bd-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_ \_ \_ 未 \_ 在復原時載入 \_ \_ WBEM MC MOF**</span><span class="sxs-lookup"><span data-stu-id="e69bd-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-116">3221225476 (0xC0000004) </span><span class="sxs-lookup"><span data-stu-id="e69bd-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-117">復原時嘗試載入 MOF %2 時，發生錯誤 %1。標記為自動回復的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="e69bd-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ 無法 \_ 啟動 \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="e69bd-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-119">3221225482 (0xC000000A) </span><span class="sxs-lookup"><span data-stu-id="e69bd-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-120">因為發生錯誤 %3，所以無法在命名空間 "%1" 中重新開機具有查詢 "%2" 的事件篩選。</span><span class="sxs-lookup"><span data-stu-id="e69bd-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="e69bd-121">在問題修正之前，無法透過此篩選傳遞事件。</span><span class="sxs-lookup"><span data-stu-id="e69bd-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC \_ 不正確 \_ 事件 \_ 提供者 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="e69bd-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-123">3221225493 (0xC0000015) </span><span class="sxs-lookup"><span data-stu-id="e69bd-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-124">事件提供者 %1 嘗試註冊語法不正確查詢 "%2"。</span><span class="sxs-lookup"><span data-stu-id="e69bd-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="e69bd-125">查詢將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e69bd-125">The query will be ignored.</span></span> <span data-ttu-id="e69bd-126">您可以使用 CIM studio 檢查 WMI 儲存機制，並更新所列提供者和查詢的永久訂閱，來修正此查詢。</span><span class="sxs-lookup"><span data-stu-id="e69bd-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="e69bd-127">如果永久訂用帳戶是使用隨附于已安裝產品的 MOF 檔案所建立，則必須聯繫應用程式廠商以修正錯誤的註冊。</span><span class="sxs-lookup"><span data-stu-id="e69bd-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM \_ MC \_ 不正確 \_ 事件 \_ 提供者 \_ \_ 內建查詢**</span><span class="sxs-lookup"><span data-stu-id="e69bd-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-129">3221225494 (0xC0000016) </span><span class="sxs-lookup"><span data-stu-id="e69bd-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-130">事件提供者 %1 嘗試在 %3 命名空間中註冊內建事件查詢 "%2"，但無法判斷其目標物件類別集合。</span><span class="sxs-lookup"><span data-stu-id="e69bd-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="e69bd-131">查詢將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e69bd-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM \_ MC \_ 事件 \_ 提供者 \_ 查詢 \_ 過於 \_ 廣泛**</span><span class="sxs-lookup"><span data-stu-id="e69bd-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-133">3221225495 (0xC0000017) </span><span class="sxs-lookup"><span data-stu-id="e69bd-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-134">事件提供者 %1 嘗試註冊 %3 命名空間中太廣泛的查詢 "%2"。</span><span class="sxs-lookup"><span data-stu-id="e69bd-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="e69bd-135">事件提供者無法提供系統所提供的事件。</span><span class="sxs-lookup"><span data-stu-id="e69bd-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="e69bd-136">查詢將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e69bd-136">The query will be ignored.</span></span> <span data-ttu-id="e69bd-137">洽詢應用程式廠商。</span><span class="sxs-lookup"><span data-stu-id="e69bd-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 WBEM MC 事件提供者查詢**</span><span class="sxs-lookup"><span data-stu-id="e69bd-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-139">3221225496 (0xC0000018) </span><span class="sxs-lookup"><span data-stu-id="e69bd-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-140">事件提供者 %1 嘗試註冊的查詢 "%2"，其目標類別 "%3" 在 %4 命名空間不存在。</span><span class="sxs-lookup"><span data-stu-id="e69bd-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="e69bd-141">查詢將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e69bd-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC \_ 事件 \_ 提供者 \_ 查詢 \_ 不是 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="e69bd-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-143">3221225497 (0xC0000019) </span><span class="sxs-lookup"><span data-stu-id="e69bd-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-144">事件提供者 %1 嘗試註冊查詢 &quot; %2， &quot; 其目標類別 &quot; %3 &quot; 不是事件類別。</span><span class="sxs-lookup"><span data-stu-id="e69bd-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="e69bd-145">查詢將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e69bd-145">The query will be ignored.</span></span> <span data-ttu-id="e69bd-146">洽詢應用程式廠商。</span><span class="sxs-lookup"><span data-stu-id="e69bd-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ 核心 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="e69bd-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-148">3221225500 (0xC000001C) </span><span class="sxs-lookup"><span data-stu-id="e69bd-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-149">無法初始化 WMI 核心或提供者子系統或事件子系統，錯誤號碼為 %1。</span><span class="sxs-lookup"><span data-stu-id="e69bd-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="e69bd-150">這可能是因為 WMI 安裝不正確、WMI 存放庫升級失敗、磁碟空間不足或記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="e69bd-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM \_ MC \_ ADAP \_ 連接 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="e69bd-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-152">3221225515 (0xC000002B) </span><span class="sxs-lookup"><span data-stu-id="e69bd-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-153">Windows Management Instrumentation ADAP 無法連接到命名空間 %1，錯誤： %2。</span><span class="sxs-lookup"><span data-stu-id="e69bd-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM \_ MC \_ ADAP \_ PERFLIB \_ PUTCLASS \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="e69bd-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-155">3221225520 (0xC0000030) </span><span class="sxs-lookup"><span data-stu-id="e69bd-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-156">Windows Management Instrumentation ADAP 無法在命名空間 %2 中儲存物件 %1，因為發生下列錯誤 %3。</span><span class="sxs-lookup"><span data-stu-id="e69bd-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ 無法 \_ \_ 新增 \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="e69bd-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-158">3221225530 (0xC000003A) </span><span class="sxs-lookup"><span data-stu-id="e69bd-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-159">Windows Management Instrumentation ADAP 無法 \_ 在 %1 中建立 Win32 效能基底類別：結果 = %2。</span><span class="sxs-lookup"><span data-stu-id="e69bd-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ 無法 \_ \_ 新增 \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="e69bd-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-161">3221225531 (0xC000003B) </span><span class="sxs-lookup"><span data-stu-id="e69bd-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-162">Windows Management Instrumentation ADAP 無法建立 Win32 \_ PerfRawData 基類 %1。</span><span class="sxs-lookup"><span data-stu-id="e69bd-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM \_ MC \_ 存放 \_ 庫 \_ 無法 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="e69bd-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-164">3221231073 (0xC00015E1) </span><span class="sxs-lookup"><span data-stu-id="e69bd-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-165">Windows Management Instrumentation 服務無法在目錄 *% windir% \\ system32 \\ wbem \\ 儲存* 機制下載入存放庫檔案。</span><span class="sxs-lookup"><span data-stu-id="e69bd-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="e69bd-166">這可能是因為存放庫檔案中的損毀、此目錄的安全性設定、磁碟空間不足或其他系統資源問題（例如記憶體不足）所造成。</span><span class="sxs-lookup"><span data-stu-id="e69bd-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="e69bd-167">如果每次電腦重新開機時都發生此錯誤，則這部電腦上的系統管理員可能需要停止 WMI 服務、檢查此資料夾和此資料夾下的檔案的安全性設定，然後執行 WMIDiag 來驗證 Windows Management Instrumentation 的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="e69bd-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ 要求 \_ \_ 拒絕加密**</span><span class="sxs-lookup"><span data-stu-id="e69bd-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-169">3221231077 (0xC00015E5) </span><span class="sxs-lookup"><span data-stu-id="e69bd-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-170">已拒絕存取 %1 命名空間，因為命名空間標記為 RequiresEncryption，但腳本或應用程式嘗試連接到此命名空間，但其驗證等級低於 **Pkt \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="e69bd-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="e69bd-171">將驗證等級變更為 **Pkt \_ 隱私權** ，然後再次執行腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="e69bd-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ 需要 \_ 加密 \_ 非同步 \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="e69bd-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-173">3221231078 (0xC00015E6) </span><span class="sxs-lookup"><span data-stu-id="e69bd-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-174">Windows Management Instrumentation 服務無法以非同步方式傳遞 %1 命名空間的結果。</span><span class="sxs-lookup"><span data-stu-id="e69bd-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="e69bd-175">命名空間會以 RequiresEncryption 標示，但 WinMgmt 無法與用戶端電腦建立安全的連線。</span><span class="sxs-lookup"><span data-stu-id="e69bd-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="e69bd-176">請確定用戶端與伺服器電腦之間有信任關係，讓用戶端能夠辨識伺服器電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="e69bd-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**已 \_ 終止 WBEM MC \_ WBEM \_ 主機 \_**</span><span class="sxs-lookup"><span data-stu-id="e69bd-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-178">3221231084 (0xC00015EC) </span><span class="sxs-lookup"><span data-stu-id="e69bd-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-179">Windows Management Instrumentation 已停止 WMIPRVSE.EXE，因為配額達到警告值。</span><span class="sxs-lookup"><span data-stu-id="e69bd-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="e69bd-180">配額： %1 值： %2 最大值： %3 WMIPRVSE PID： %4。</span><span class="sxs-lookup"><span data-stu-id="e69bd-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="e69bd-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-182">3221231086 (0xC00015EE) </span><span class="sxs-lookup"><span data-stu-id="e69bd-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-183">在服務啟動期間，Windows Management Instrumentation 服務無法找到存放庫檔案。</span><span class="sxs-lookup"><span data-stu-id="e69bd-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="e69bd-184">系統會根據自動復原機制來建立新的存放庫。</span><span class="sxs-lookup"><span data-stu-id="e69bd-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**\_ \_ \_ 已成功啟動 WBEM MC WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="e69bd-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-186">3221231087 (0xC00015EF) </span><span class="sxs-lookup"><span data-stu-id="e69bd-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-187">Windows Management Instrumentation 服務已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="e69bd-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ 核心 \_ PSS \_ ESS 已 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="e69bd-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-189">3221231089 (0xC00015F1) </span><span class="sxs-lookup"><span data-stu-id="e69bd-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-190">已成功初始化 Windows Management Instrumentation 服務子系統。</span><span class="sxs-lookup"><span data-stu-id="e69bd-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM \_ MC \_ WBEM \_ 服務 \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="e69bd-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-192">3221225501 (0xC000001D) </span><span class="sxs-lookup"><span data-stu-id="e69bd-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-193">嘗試初始化 Windows Management Instrumentation 服務時，傳回錯誤號碼 %1。</span><span class="sxs-lookup"><span data-stu-id="e69bd-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="e69bd-194">這可能是因為 WMI 安裝不正確、WMI 存放庫升級失敗、磁碟空間不足或記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="e69bd-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e69bd-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**已 \_ 重建 WBEM MC \_ WBEM \_ 儲存 \_ 機制**</span><span class="sxs-lookup"><span data-stu-id="e69bd-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69bd-196">3221231088 (0xC00015F0) </span><span class="sxs-lookup"><span data-stu-id="e69bd-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="e69bd-197">已使用自動復原機制成功重新建立 Windows Management Instrumentation 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e69bd-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e69bd-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="e69bd-198">Requirements</span></span>



| <span data-ttu-id="e69bd-199">需求</span><span class="sxs-lookup"><span data-stu-id="e69bd-199">Requirement</span></span> | <span data-ttu-id="e69bd-200">值</span><span class="sxs-lookup"><span data-stu-id="e69bd-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e69bd-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e69bd-201">Minimum supported client</span></span><br/> | <span data-ttu-id="e69bd-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e69bd-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e69bd-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e69bd-203">Minimum supported server</span></span><br/> | <span data-ttu-id="e69bd-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e69bd-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e69bd-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e69bd-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69bd-206">WMI 事件</span><span class="sxs-lookup"><span data-stu-id="e69bd-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

<span data-ttu-id="e69bd-207">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="e69bd-207">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> </dl>

 

 




