---
title: WER 設定
description: 自訂問題報告體驗的設定。 所有這些設定都可以使用群組原則來設定。 您也可以在 Windows 7 和 Windows 8 的 [行動中心] 中變更部分。 針對 Windows 10，請使用 [設定] 中的 [搜尋] 功能，找出 View advanced 系統設定。
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows 錯誤報告 Windows 錯誤報告，設定
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/13/2021
ms.locfileid: "106992697"
---
# <a name="wer-settings"></a><span data-ttu-id="56a0c-107">WER 設定</span><span class="sxs-lookup"><span data-stu-id="56a0c-107">WER Settings</span></span>

<span data-ttu-id="56a0c-108">Windows 錯誤報告 (WER) 提供許多設定來自訂問題報告體驗。</span><span class="sxs-lookup"><span data-stu-id="56a0c-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="56a0c-109">所有這些設定都可以使用群組原則來設定。</span><span class="sxs-lookup"><span data-stu-id="56a0c-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="56a0c-110">您也可以在 Windows 7 和 Windows 8 的 [ **行動中心** ] 中變更部分。</span><span class="sxs-lookup"><span data-stu-id="56a0c-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="56a0c-111">針對 Windows 10，請使用 [設定] 中的 [搜尋] 功能，找出 **View advanced 系統設定**。</span><span class="sxs-lookup"><span data-stu-id="56a0c-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="56a0c-112">WER 設定位於下列其中一個登錄子機碼中：</span><span class="sxs-lookup"><span data-stu-id="56a0c-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="56a0c-113">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **Windows 錯誤報告**</span><span class="sxs-lookup"><span data-stu-id="56a0c-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="56a0c-114">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **Windows 錯誤報告**</span><span class="sxs-lookup"><span data-stu-id="56a0c-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="56a0c-115">Windows 錯誤報告子機碼</span><span class="sxs-lookup"><span data-stu-id="56a0c-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="56a0c-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span><span class="sxs-lookup"><span data-stu-id="56a0c-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-117">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-118">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="56a0c-119">0-停用資料略過節流。</span><span class="sxs-lookup"><span data-stu-id="56a0c-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="56a0c-120">如果許可已停用或未設定為原則設定，則 WER 預設會節流資料。</span><span class="sxs-lookup"><span data-stu-id="56a0c-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="56a0c-121">如果報表包含相同事件種類的相關資料，則 WER 不會上傳多個 CAB 檔。</span><span class="sxs-lookup"><span data-stu-id="56a0c-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="56a0c-122">1-啟用資料略過節流。</span><span class="sxs-lookup"><span data-stu-id="56a0c-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="56a0c-123">WER 不會對資料進行節流。</span><span class="sxs-lookup"><span data-stu-id="56a0c-123">WER does not throttle data.</span></span> <span data-ttu-id="56a0c-124">WER 會上傳額外的封包檔，其可能包含與先前上傳報表相同之事件種類的相關資料。</span><span class="sxs-lookup"><span data-stu-id="56a0c-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="56a0c-125">是否要啟用 WER 用戶端資料節流的略過</span><span class="sxs-lookup"><span data-stu-id="56a0c-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span><span class="sxs-lookup"><span data-stu-id="56a0c-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-127">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-127">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-128">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-128">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-129">1-只有在 Windows 7) 上 (預設參數</span><span class="sxs-lookup"><span data-stu-id="56a0c-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="56a0c-130">2-Windows Vista) 上的所有資料 (預設值</span><span class="sxs-lookup"><span data-stu-id="56a0c-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="56a0c-131">是否只封存參數或所有資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**同意 \\ DefaultConsent**</span><span class="sxs-lookup"><span data-stu-id="56a0c-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-133">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-133">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-134">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-134">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-135">1-一律詢問 (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="56a0c-136">2-僅限參數</span><span class="sxs-lookup"><span data-stu-id="56a0c-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="56a0c-137">3-參數和安全資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="56a0c-138">4-所有資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="56a0c-139">預設同意選項</span><span class="sxs-lookup"><span data-stu-id="56a0c-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**同意 \\ DefaultOverrideBehavior**</span><span class="sxs-lookup"><span data-stu-id="56a0c-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-141">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-141">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-142">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-142">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-143">0-垂直同意會覆寫預設的同意 (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="56a0c-144">1-預設同意將覆寫應用程式特定同意</span><span class="sxs-lookup"><span data-stu-id="56a0c-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="56a0c-145">預設同意是否覆寫垂直同意</span><span class="sxs-lookup"><span data-stu-id="56a0c-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**同意 \\ \[ VerticalName\]**</span><span class="sxs-lookup"><span data-stu-id="56a0c-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-147">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-148">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-148">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-149">1-一律詢問 (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="56a0c-150">2-僅限參數</span><span class="sxs-lookup"><span data-stu-id="56a0c-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="56a0c-151">3-參數和安全資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="56a0c-152">4-所有資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="56a0c-153">WER 外掛程式的同意選擇</span><span class="sxs-lookup"><span data-stu-id="56a0c-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span><span class="sxs-lookup"><span data-stu-id="56a0c-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-155">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="56a0c-155">**REG\_SZ**</span></span>

<span data-ttu-id="56a0c-156">目錄路徑</span><span class="sxs-lookup"><span data-stu-id="56a0c-156">The directory path</span></span>

<span data-ttu-id="56a0c-157">伺服器上的目標目錄</span><span class="sxs-lookup"><span data-stu-id="56a0c-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span><span class="sxs-lookup"><span data-stu-id="56a0c-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-159">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-159">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-160">埠號碼</span><span class="sxs-lookup"><span data-stu-id="56a0c-160">The port number</span></span>

<span data-ttu-id="56a0c-161">要與公司伺服器搭配使用的埠號碼</span><span class="sxs-lookup"><span data-stu-id="56a0c-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span><span class="sxs-lookup"><span data-stu-id="56a0c-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-163">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="56a0c-163">**REG\_SZ**</span></span>

<span data-ttu-id="56a0c-164">伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="56a0c-164">The name of the server</span></span>

<span data-ttu-id="56a0c-165">公司伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="56a0c-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span><span class="sxs-lookup"><span data-stu-id="56a0c-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-167">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-167">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-168">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-168">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-169">0-沒有 (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="56a0c-170">1 - 是</span><span class="sxs-lookup"><span data-stu-id="56a0c-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="56a0c-171">是否要使用 Windows 整合式驗證</span><span class="sxs-lookup"><span data-stu-id="56a0c-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span><span class="sxs-lookup"><span data-stu-id="56a0c-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-173">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-173">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-174">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-174">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-175">0-沒有 (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="56a0c-176">1 - 是</span><span class="sxs-lookup"><span data-stu-id="56a0c-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="56a0c-177">是否要使用 SSL</span><span class="sxs-lookup"><span data-stu-id="56a0c-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ ExeName \] (\[ \] 以 .exe 檔案名的實際名稱取代 "ExeName"，例如 "notepad.exe" )**</span><span class="sxs-lookup"><span data-stu-id="56a0c-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-179">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-180">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="56a0c-181">0-具有可執行映射名稱 **\[ ExeName \]** 的處理常式不需要使用者選擇 [ **Debug** ] 或 [**繼續**] (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="56a0c-182">1-具有可執行映射名稱 **\[ ExeName \]** 的處理常式需要使用者選擇 [ **Debug** ] 或 [ **Continue** ]</span><span class="sxs-lookup"><span data-stu-id="56a0c-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="56a0c-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* ( " \* " 是常值名稱)**</span><span class="sxs-lookup"><span data-stu-id="56a0c-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-184">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-184">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-185">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="56a0c-186">0-在 [設定 **DebugApplications \\ \[ \] ExeName** ] 中明確指定的所有進程都不需要使用者選擇 [ **Debug** ] 或 [**繼續**] (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="56a0c-187">1-在 [設定 **DebugApplications \\ \[ \] ExeName** ] 中明確指定的所有進程都需要使用者選擇 [ **Debug** ] 或 [ **Continue** ]</span><span class="sxs-lookup"><span data-stu-id="56a0c-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="56a0c-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span><span class="sxs-lookup"><span data-stu-id="56a0c-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-189">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-189">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-190">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-190">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-191">0 - 已啟用</span><span class="sxs-lookup"><span data-stu-id="56a0c-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="56a0c-192">1 - 已停用</span><span class="sxs-lookup"><span data-stu-id="56a0c-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="56a0c-193">啟用或停用封存</span><span class="sxs-lookup"><span data-stu-id="56a0c-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**</span><span class="sxs-lookup"><span data-stu-id="56a0c-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-195">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-195">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-196">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-196">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-197">啟用 0 (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="56a0c-198">1 - 已停用</span><span class="sxs-lookup"><span data-stu-id="56a0c-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="56a0c-199">啟用或停用 WER</span><span class="sxs-lookup"><span data-stu-id="56a0c-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span><span class="sxs-lookup"><span data-stu-id="56a0c-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-201">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-201">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-202">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-202">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-203">0 - 已啟用</span><span class="sxs-lookup"><span data-stu-id="56a0c-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="56a0c-204">1 - 已停用</span><span class="sxs-lookup"><span data-stu-id="56a0c-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="56a0c-205">啟用或停用報表佇列</span><span class="sxs-lookup"><span data-stu-id="56a0c-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="56a0c-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-207">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-207">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-208">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-208">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-209">0-UI (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="56a0c-210">1-沒有 UI</span><span class="sxs-lookup"><span data-stu-id="56a0c-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="56a0c-211">啟用或停用 WER UI</span><span class="sxs-lookup"><span data-stu-id="56a0c-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span><span class="sxs-lookup"><span data-stu-id="56a0c-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-213">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-213">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-214">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-214">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-215">0-傳送 (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="56a0c-216">1-不要傳送</span><span class="sxs-lookup"><span data-stu-id="56a0c-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="56a0c-217">是否防止傳送第二層資料</span><span class="sxs-lookup"><span data-stu-id="56a0c-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications \\ \[ 應用程式名稱\]**</span><span class="sxs-lookup"><span data-stu-id="56a0c-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-219">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="56a0c-219">**REG\_SZ**</span></span>

<span data-ttu-id="56a0c-220">使用 [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="56a0c-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="56a0c-221">排除的應用程式清單</span><span class="sxs-lookup"><span data-stu-id="56a0c-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span><span class="sxs-lookup"><span data-stu-id="56a0c-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-223">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-223">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-224">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-224">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-225">0-沒有 (預設值) </span><span class="sxs-lookup"><span data-stu-id="56a0c-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="56a0c-226">1 - 是</span><span class="sxs-lookup"><span data-stu-id="56a0c-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="56a0c-227">是否要將所有報表傳送至使用者的佇列</span><span class="sxs-lookup"><span data-stu-id="56a0c-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\DumpFolder** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpFolder**</span><span class="sxs-lookup"><span data-stu-id="56a0c-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-229">**REG \_ EXPAND \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="56a0c-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="56a0c-230">目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="56a0c-230">The directory path.</span></span> <span data-ttu-id="56a0c-231">預設值為% LOCALAPPDATA% \\ CrashDumps。</span><span class="sxs-lookup"><span data-stu-id="56a0c-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="56a0c-232">如果未使用預設值，則應用程式必須確定資料夾有足夠的 ACL。</span><span class="sxs-lookup"><span data-stu-id="56a0c-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="56a0c-233">**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="56a0c-234">請注意，此行為隨著 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 而變更。</span><span class="sxs-lookup"><span data-stu-id="56a0c-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="56a0c-235">要儲存傾印檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="56a0c-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="56a0c-236">請注意，每個進程的設定會覆寫任何存在的全域設定。如需詳細資訊，請參閱 [收集 User-Mode](collecting-user-mode-dumps.md)傾印。</span><span class="sxs-lookup"><span data-stu-id="56a0c-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="56a0c-237">**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。</span><span class="sxs-lookup"><span data-stu-id="56a0c-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\DumpCount** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpCount**</span><span class="sxs-lookup"><span data-stu-id="56a0c-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-239">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-239">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-240">最大數目。</span><span class="sxs-lookup"><span data-stu-id="56a0c-240">The maximum number.</span></span> <span data-ttu-id="56a0c-241">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="56a0c-241">The default is 10.</span></span> <span data-ttu-id="56a0c-242">當超過最大值時，資料夾中最舊的傾印檔案將會取代為新的傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="56a0c-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="56a0c-243">**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="56a0c-244">請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。</span><span class="sxs-lookup"><span data-stu-id="56a0c-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="56a0c-245">資料夾中傾印檔案的最大數目。</span><span class="sxs-lookup"><span data-stu-id="56a0c-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="56a0c-246">**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。</span><span class="sxs-lookup"><span data-stu-id="56a0c-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\DumpType** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpType**</span><span class="sxs-lookup"><span data-stu-id="56a0c-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-248">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-248">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-249">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-249">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-250">0-自訂傾印</span><span class="sxs-lookup"><span data-stu-id="56a0c-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="56a0c-251">1-小型傾印 (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="56a0c-252">2-完整傾印</span><span class="sxs-lookup"><span data-stu-id="56a0c-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="56a0c-253">**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="56a0c-254">請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。</span><span class="sxs-lookup"><span data-stu-id="56a0c-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="56a0c-255">傾印類型。</span><span class="sxs-lookup"><span data-stu-id="56a0c-255">The dump type.</span></span>

<span data-ttu-id="56a0c-256">**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。</span><span class="sxs-lookup"><span data-stu-id="56a0c-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\CustomDumpFlags** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ CustomDumpFlags**</span><span class="sxs-lookup"><span data-stu-id="56a0c-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-258">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-258">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-259">小型傾印 [**\_ 類型**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) 列舉中的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="56a0c-260">預設值為 {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}。</span><span class="sxs-lookup"><span data-stu-id="56a0c-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="56a0c-261">**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="56a0c-262">請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。</span><span class="sxs-lookup"><span data-stu-id="56a0c-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="56a0c-263">要使用的自訂傾印選項。</span><span class="sxs-lookup"><span data-stu-id="56a0c-263">The custom dump options to be used.</span></span> <span data-ttu-id="56a0c-264">只有當 **DumpType** 設為0時，才會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="56a0c-265">**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。</span><span class="sxs-lookup"><span data-stu-id="56a0c-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span><span class="sxs-lookup"><span data-stu-id="56a0c-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-267">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-267">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-268">可能的值：</span><span class="sxs-lookup"><span data-stu-id="56a0c-268">Possible values:</span></span><dl> <dd><span data-ttu-id="56a0c-269">0–已啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="56a0c-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="56a0c-270">1–已停用</span><span class="sxs-lookup"><span data-stu-id="56a0c-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="56a0c-271">啟用或停用記錄</span><span class="sxs-lookup"><span data-stu-id="56a0c-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span><span class="sxs-lookup"><span data-stu-id="56a0c-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-273">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-273">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-274">可能值的範圍：1–5000。</span><span class="sxs-lookup"><span data-stu-id="56a0c-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="56a0c-275">預設值是 1000。</span><span class="sxs-lookup"><span data-stu-id="56a0c-275">The default is 1000.</span></span>

<span data-ttu-id="56a0c-276">檔案中封存的大小上限</span><span class="sxs-lookup"><span data-stu-id="56a0c-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span><span class="sxs-lookup"><span data-stu-id="56a0c-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-278">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-278">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-279">可能值的範圍： 1-500。</span><span class="sxs-lookup"><span data-stu-id="56a0c-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="56a0c-280">預設值為 50。</span><span class="sxs-lookup"><span data-stu-id="56a0c-280">The default is 50.</span></span>

<span data-ttu-id="56a0c-281">佇列的大小上限</span><span class="sxs-lookup"><span data-stu-id="56a0c-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span><span class="sxs-lookup"><span data-stu-id="56a0c-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-283">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-283">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-284">天數</span><span class="sxs-lookup"><span data-stu-id="56a0c-284">Number of days</span></span>

<span data-ttu-id="56a0c-285">要檢查解決方案的使用者提醒間隔（以天為單位）</span><span class="sxs-lookup"><span data-stu-id="56a0c-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules！ \[ pwszOutOfProcessCallbackDll 名稱，包括路徑\]**</span><span class="sxs-lookup"><span data-stu-id="56a0c-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-287">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-287">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-288">系統會忽略值的內容。</span><span class="sxs-lookup"><span data-stu-id="56a0c-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="56a0c-289">值的名稱是用來提取 pwszOutOfProcessCallbackDll 值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="56a0c-290">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="56a0c-291">WER 即時核心報告設定</span><span class="sxs-lookup"><span data-stu-id="56a0c-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="56a0c-292">接下來會說明 WER 的即時核心報告設定，兩者都位於下列登錄子機碼底下：</span><span class="sxs-lookup"><span data-stu-id="56a0c-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="56a0c-293">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="56a0c-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="56a0c-294">FullLiveKernelReports 子機碼</span><span class="sxs-lookup"><span data-stu-id="56a0c-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="56a0c-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="56a0c-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-296">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-296">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-297">每個元件可以建立完整即時傾印的頻率，以小時為單位的閾值 () 。</span><span class="sxs-lookup"><span data-stu-id="56a0c-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="56a0c-298">此值必須大於或等於 **SystemThrottleThreshold**。</span><span class="sxs-lookup"><span data-stu-id="56a0c-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="56a0c-299">將兩者設定為零 (0) 將會停用所有以時間為基礎的節流。</span><span class="sxs-lookup"><span data-stu-id="56a0c-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="56a0c-300">預設值為 168 (7 天) 。</span><span class="sxs-lookup"><span data-stu-id="56a0c-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span><span class="sxs-lookup"><span data-stu-id="56a0c-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-302">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-302">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-303">在任何指定時間可在磁片上的完整即時傾印數目上限。</span><span class="sxs-lookup"><span data-stu-id="56a0c-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="56a0c-304">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="56a0c-304">The default is 1.</span></span> <span data-ttu-id="56a0c-305">將此值設定為零 (0) 將會停用即時傾印功能。</span><span class="sxs-lookup"><span data-stu-id="56a0c-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span><span class="sxs-lookup"><span data-stu-id="56a0c-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-307">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-307">**REG\_QWORD**</span></span>

<span data-ttu-id="56a0c-308">[SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ，表示系統或特定 >reporttype 的上次完整即時報告時間。</span><span class="sxs-lookup"><span data-stu-id="56a0c-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="56a0c-309">這是用來計算是否已滿足原則閾值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="56a0c-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="56a0c-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-311">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="56a0c-311">**REG\_DWORD**</span></span>

<span data-ttu-id="56a0c-312">系統上的任何元件可以建立完整的即時傾印，以小時為單位的閾值 () 。</span><span class="sxs-lookup"><span data-stu-id="56a0c-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="56a0c-313">預設值為 120 (5 天) 。</span><span class="sxs-lookup"><span data-stu-id="56a0c-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="56a0c-314">LiveKernelReports 子機碼</span><span class="sxs-lookup"><span data-stu-id="56a0c-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="56a0c-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span><span class="sxs-lookup"><span data-stu-id="56a0c-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-316">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="56a0c-316">**REG\_SZ**</span></span>


<span data-ttu-id="56a0c-317">即時核心報告的重新導向儲存位置。</span><span class="sxs-lookup"><span data-stu-id="56a0c-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="56a0c-318">預設位置為%systemroot%\LiveKernelReports。</span><span class="sxs-lookup"><span data-stu-id="56a0c-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="56a0c-319">此值必須是有效的路徑。</span><span class="sxs-lookup"><span data-stu-id="56a0c-319">This value must be a valid path.</span></span> <span data-ttu-id="56a0c-320">路徑必須是 NT 路徑格式。</span><span class="sxs-lookup"><span data-stu-id="56a0c-320">The path must be in NT path format.</span></span> <span data-ttu-id="56a0c-321">例如， \? ？ \c： \LiveDumpsFolder。</span><span class="sxs-lookup"><span data-stu-id="56a0c-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="56a0c-322">如需路徑格式的詳細資訊，請參閱  [Windows 系統上的檔案路徑格式](/dotnet/standard/io/file-path-formats)。</span><span class="sxs-lookup"><span data-stu-id="56a0c-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="56a0c-323">相關主題</span><span class="sxs-lookup"><span data-stu-id="56a0c-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a0c-324">WER 參考</span><span class="sxs-lookup"><span data-stu-id="56a0c-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
