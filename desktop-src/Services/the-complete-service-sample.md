---
description: 深入瞭解：完整的服務範例
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: 完整的服務範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980453"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="66cda-103">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="66cda-103">The Complete Service Sample</span></span>

<span data-ttu-id="66cda-104">本節中的主題會形成完整的服務範例：</span><span class="sxs-lookup"><span data-stu-id="66cda-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="66cda-105">[Sample.mc](sample-mc.md) (包含錯誤訊息) </span><span class="sxs-lookup"><span data-stu-id="66cda-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="66cda-106">[.Svc .cpp](svc-cpp.md) (包含服務程式代碼) </span><span class="sxs-lookup"><span data-stu-id="66cda-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="66cda-107">[SvcConfig .cpp](svcconfig-cpp.md) (包含服務設定程式碼) </span><span class="sxs-lookup"><span data-stu-id="66cda-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="66cda-108">[SvcControl .cpp](svccontrol-cpp.md) (包含服務控制程式代碼) </span><span class="sxs-lookup"><span data-stu-id="66cda-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="66cda-109">建置服務</span><span class="sxs-lookup"><span data-stu-id="66cda-109">Building the Service</span></span>

<span data-ttu-id="66cda-110">下列程式描述如何建立服務並註冊事件訊息 DLL。</span><span class="sxs-lookup"><span data-stu-id="66cda-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="66cda-111">**若要建立服務並註冊事件訊息 DLL**</span><span class="sxs-lookup"><span data-stu-id="66cda-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="66cda-112">使用下列步驟，從 Sample.mc 建立訊息 DLL：</span><span class="sxs-lookup"><span data-stu-id="66cda-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="66cda-113">**mc-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="66cda-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="66cda-114">**rc-r 範例 .rc**</span><span class="sxs-lookup"><span data-stu-id="66cda-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="66cda-115">**程式庫-noentry -out:sample.dll 範例 .res**</span><span class="sxs-lookup"><span data-stu-id="66cda-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="66cda-116">分別從 .Svc、SvcConfig .cpp 和 SvcControl 建立 Svc.exe、SvcConfig.exe 和 SvcControl.exe。</span><span class="sxs-lookup"><span data-stu-id="66cda-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="66cda-117">建立登錄機碼 **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 服務 \\ EventLog \\ 應用程式 \\ SvcName** ，並將下列登錄值新增至此索引鍵。</span><span class="sxs-lookup"><span data-stu-id="66cda-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="66cda-118">值</span><span class="sxs-lookup"><span data-stu-id="66cda-118">Value</span></span>                              | <span data-ttu-id="66cda-119">類型</span><span class="sxs-lookup"><span data-stu-id="66cda-119">Type</span></span>       | <span data-ttu-id="66cda-120">Description</span><span class="sxs-lookup"><span data-stu-id="66cda-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="66cda-121">**EventMessageFile**  = *dll \_ 路徑*</span><span class="sxs-lookup"><span data-stu-id="66cda-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="66cda-122">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="66cda-122">REG\_SZ</span></span>    | <span data-ttu-id="66cda-123">僅含資源的 DLL 路徑，其中包含服務可寫入事件記錄檔中的字串。</span><span class="sxs-lookup"><span data-stu-id="66cda-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="66cda-124">**TypesSupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="66cda-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="66cda-125">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="66cda-125">REG\_DWORD</span></span> | <span data-ttu-id="66cda-126">指定支援的事件種類的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="66cda-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="66cda-127">值0x000000007 表示支援所有類型。</span><span class="sxs-lookup"><span data-stu-id="66cda-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="66cda-128">測試服務</span><span class="sxs-lookup"><span data-stu-id="66cda-128">Testing the Service</span></span>

<span data-ttu-id="66cda-129">下列程式說明如何測試服務。</span><span class="sxs-lookup"><span data-stu-id="66cda-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="66cda-130">**若要測試服務**</span><span class="sxs-lookup"><span data-stu-id="66cda-130">**To test the service**</span></span>

1.  <span data-ttu-id="66cda-131">在主控台中，啟動 [ **服務** ] 應用程式。</span><span class="sxs-lookup"><span data-stu-id="66cda-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="66cda-132"> (在下列步驟中，在執行修改 **服務** 應用程式中資訊的命令之後，使用 F5 鍵重新整理顯示。 ) </span><span class="sxs-lookup"><span data-stu-id="66cda-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="66cda-133">執行下列命令以安裝服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="66cda-134">**svc 安裝**</span><span class="sxs-lookup"><span data-stu-id="66cda-134">**svc install**</span></span>

    <span data-ttu-id="66cda-135">如果作業成功，服務就會將「服務安裝成功」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="66cda-136">如果服務安裝成功，服務就會顯示在 [ **服務** ] 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="66cda-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="66cda-137">請注意，[ **名稱** ] 設定為 "SvcName"、 **描述** 和 **狀態** 為空白，而 [ **啟動類型** ] 設定為 [手動]。</span><span class="sxs-lookup"><span data-stu-id="66cda-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="66cda-138">執行下列命令來啟動服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="66cda-139">**svccontrol 開始 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="66cda-140">如果作業成功，服務控制程式會寫入「服務開始擱置中 ...」然後「服務已成功啟動」至主控台。</span><span class="sxs-lookup"><span data-stu-id="66cda-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="66cda-141">否則，程式會將錯誤訊息寫入主控台。</span><span class="sxs-lookup"><span data-stu-id="66cda-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="66cda-142">如果服務成功啟動，則 **狀態** 會設定為「已啟動」。</span><span class="sxs-lookup"><span data-stu-id="66cda-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="66cda-143">[*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)函式中的程式碼是由 SCM 執行。</span><span class="sxs-lookup"><span data-stu-id="66cda-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="66cda-144">如果發生錯誤，服務會將錯誤訊息寫入至事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="66cda-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="66cda-145">此訊息包含失敗的函式名稱，以及失敗時傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="66cda-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="66cda-146">執行下列命令以更新服務描述：</span><span class="sxs-lookup"><span data-stu-id="66cda-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="66cda-147">**svcconfig 描述 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="66cda-148">如果作業成功，服務設定程式會將「服務描述更新成功」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="66cda-149">如果更新成功， **描述** 會設定為「這是測試描述」。</span><span class="sxs-lookup"><span data-stu-id="66cda-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="66cda-150">執行下列命令來查詢服務設定：</span><span class="sxs-lookup"><span data-stu-id="66cda-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="66cda-151">**svcconfig 查詢 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="66cda-152">如果作業成功，服務設定程式會將服務設定資訊寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="66cda-153">執行下列命令來變更服務 DACL：</span><span class="sxs-lookup"><span data-stu-id="66cda-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="66cda-154">**svccontrol dacl SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="66cda-155">如果作業成功，服務設定程式會將「服務 DACL 更新成功」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="66cda-156">執行下列命令以停用服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="66cda-157">**svcconfig 停用 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="66cda-158">如果作業成功，服務設定程式會將「服務已成功停用」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="66cda-159">如果服務已成功停用， **啟動類型** 會設定為「已停用」。</span><span class="sxs-lookup"><span data-stu-id="66cda-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="66cda-160">執行下列命令以啟用服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="66cda-161">**svcconfig 啟用 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="66cda-162">如果作業成功，服務設定程式會將「已成功啟用服務」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="66cda-163">如果成功啟用服務，[ **啟動類型** ] 設定為 [手動]。</span><span class="sxs-lookup"><span data-stu-id="66cda-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="66cda-164">執行下列命令來停止服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="66cda-165">**svccontrol 停止 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="66cda-166">如果作業成功，服務控制程式會將 "Service stop pending ..." 寫入然後「服務已成功停止」至主控台。</span><span class="sxs-lookup"><span data-stu-id="66cda-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="66cda-167">否則，程式會將錯誤訊息寫入主控台。</span><span class="sxs-lookup"><span data-stu-id="66cda-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="66cda-168">如果服務成功停止， **狀態** 會是空白。</span><span class="sxs-lookup"><span data-stu-id="66cda-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="66cda-169">如果服務無法停止，服務控制程式會將錯誤訊息寫入至事件記錄檔，其中包含失敗的函式名稱，以及失敗時傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="66cda-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="66cda-170">執行下列命令來刪除服務：</span><span class="sxs-lookup"><span data-stu-id="66cda-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="66cda-171">**svcconfig 刪除 SvcName**</span><span class="sxs-lookup"><span data-stu-id="66cda-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="66cda-172">如果作業成功，服務設定程式會將「服務刪除成功」寫入主控台，否則會傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66cda-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="66cda-173">如果成功刪除服務， **服務** 應用程式就不會再顯示該服務。</span><span class="sxs-lookup"><span data-stu-id="66cda-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="66cda-174"> (請注意，如果您嘗試刪除未停止的服務，該作業會成功，但 [ **啟動類型** ] 設定為 [已停用]，而在系統重新開機時或使用工作管理員終止服務時，會刪除服務專案。 ) </span><span class="sxs-lookup"><span data-stu-id="66cda-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="66cda-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="66cda-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66cda-176">使用服務</span><span class="sxs-lookup"><span data-stu-id="66cda-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
