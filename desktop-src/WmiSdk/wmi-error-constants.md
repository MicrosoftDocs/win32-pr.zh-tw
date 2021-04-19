---
description: 如果發生錯誤，WMI 會以 HRESULT 值傳回錯誤碼。 腳本、c + + 應用程式或 Wmic 可能會傳回這些程式碼。
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: 'WMI 錯誤常數 (WbemCli) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974377"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="004fe-104">WMI 錯誤常數</span><span class="sxs-lookup"><span data-stu-id="004fe-104">WMI Error Constants</span></span>

<span data-ttu-id="004fe-105">如果發生錯誤，WMI 會以 **HRESULT** 值傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="004fe-106">腳本、c + + 應用程式或 [**Wmic**](wmic.md)可能會傳回這些程式碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="004fe-107">下列檔的目標是開發人員和 IT 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="004fe-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="004fe-108">如果您是遇到關於 WMI 的錯誤訊息的使用者，您應該移至 [Microsoft 支援服務](https://support.microsoft.com/) 並搜尋錯誤訊息上所看到的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="004fe-109">如需有關疑難排解 WMI 腳本和 WMI 服務問題的詳細資訊，請參閱 [Wmi 無法運作！](/previous-versions/tn-archive/ff406382(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="004fe-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="004fe-110">如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。</span><span class="sxs-lookup"><span data-stu-id="004fe-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="004fe-111">失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="004fe-112">在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="004fe-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="004fe-113">若要取得問題來源的詳細資訊，您可以下載並執行 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) 診斷命令列工具。</span><span class="sxs-lookup"><span data-stu-id="004fe-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="004fe-114">這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。</span><span class="sxs-lookup"><span data-stu-id="004fe-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="004fe-115">報表也會協助 Microsoft 支援服務協助您。</span><span class="sxs-lookup"><span data-stu-id="004fe-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="004fe-116">您可以在 [這裡](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)下載 WMI Diagnosis Utility。</span><span class="sxs-lookup"><span data-stu-id="004fe-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="004fe-117">WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。</span><span class="sxs-lookup"><span data-stu-id="004fe-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="004fe-118">您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。</span><span class="sxs-lookup"><span data-stu-id="004fe-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="004fe-119">例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="004fe-120">下列清單列出一些常見的錯誤範圍。</span><span class="sxs-lookup"><span data-stu-id="004fe-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="004fe-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="004fe-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="004fe-122">源自 WMI 本身的錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="004fe-123">特定 WMI 作業失敗，因為</span><span class="sxs-lookup"><span data-stu-id="004fe-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="004fe-124">要求中發生錯誤，例如 WQL 查詢失敗或帳戶沒有正確的許可權。</span><span class="sxs-lookup"><span data-stu-id="004fe-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="004fe-125">WMI 基礎結構問題，例如不正確的 CIM 或 DCOM 註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="004fe-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="004fe-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="004fe-127">源自核心作業系統的錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="004fe-128">WMI 可能會因為外部失敗而傳回此類型的錯誤，例如 DCOM 安全性失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="004fe-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="004fe-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="004fe-130">源自 DCOM 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-130">Errors originating in DCOM.</span></span> <span data-ttu-id="004fe-131">例如，遠端電腦的作業 DCOM 設定可能不正確。</span><span class="sxs-lookup"><span data-stu-id="004fe-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="004fe-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="004fe-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="004fe-133">源自 ADSI (Active Directory 服務介面的錯誤) 或 LDAP (輕量型目錄存取協定) ，例如，使用 WMI Active Directory 提供者時 Active Directory 存取失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="004fe-134">WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。</span><span class="sxs-lookup"><span data-stu-id="004fe-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="004fe-135">您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。</span><span class="sxs-lookup"><span data-stu-id="004fe-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="004fe-136">例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="004fe-137">在 c + + 中，您可以呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 並指定 **C： \\ Windows \\ System32 \\ wbem \\wmiutils.dll** 作為訊息模組。</span><span class="sxs-lookup"><span data-stu-id="004fe-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="004fe-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-139">2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="004fe-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-140">呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**\_ \_ 找不到 WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-142">2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="004fe-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-143">找不到物件。</span><span class="sxs-lookup"><span data-stu-id="004fe-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E \_ \_ 拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="004fe-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-145">2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="004fe-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-146">目前的使用者沒有執行此動作的許可權。</span><span class="sxs-lookup"><span data-stu-id="004fe-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM \_ E \_ 提供者 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-148">2147749892 (0x80041004) </span><span class="sxs-lookup"><span data-stu-id="004fe-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-149">在初始化期間，提供者在某些時間失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="004fe-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-151">2147749893 (0x80041005) </span><span class="sxs-lookup"><span data-stu-id="004fe-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-152">發生類型不符的情況。</span><span class="sxs-lookup"><span data-stu-id="004fe-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ 記憶體不足 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-154">2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="004fe-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-155">記憶體不足，無法運作。</span><span class="sxs-lookup"><span data-stu-id="004fe-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E \_ 不正確 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="004fe-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-157">2147749895 (0x80041007) </span><span class="sxs-lookup"><span data-stu-id="004fe-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-158">[**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM \_ E \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="004fe-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-160">2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="004fe-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-161">呼叫的其中一個參數不正確。</span><span class="sxs-lookup"><span data-stu-id="004fe-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="004fe-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-163">2147749897 (0x80041009) </span><span class="sxs-lookup"><span data-stu-id="004fe-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-164">資源（通常是遠端伺服器）目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ 重大 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="004fe-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-166">2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="004fe-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-167">發生內部、重大和非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="004fe-168">向 Microsoft 技術支援人員回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ 不正確 \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="004fe-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-170">2147749899 (0x8004100B) </span><span class="sxs-lookup"><span data-stu-id="004fe-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-171">一個或多個網路封包在遠端工作階段 (Session) 期間損毀。</span><span class="sxs-lookup"><span data-stu-id="004fe-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ 不支援 WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="004fe-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-173">2147749900 (0x8004100C) </span><span class="sxs-lookup"><span data-stu-id="004fe-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-174">不支援功能或操作。</span><span class="sxs-lookup"><span data-stu-id="004fe-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ 不正確 \_ 超類**</span><span class="sxs-lookup"><span data-stu-id="004fe-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-176">2147749901 (0x8004100D) </span><span class="sxs-lookup"><span data-stu-id="004fe-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-177">指定的父類別無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ 不正確 \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="004fe-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-179">2147749902 (0x8004100E) </span><span class="sxs-lookup"><span data-stu-id="004fe-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-180">找不到指定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="004fe-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ 不正確 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="004fe-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-182">2147749903 (0x8004100F) </span><span class="sxs-lookup"><span data-stu-id="004fe-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-183">指定的實例無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ E \_ 無效 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="004fe-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-185">2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="004fe-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-186">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_ \_ \_ 找不到 WBEM E 提供者 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-188">2147749905 (0x80041011) </span><span class="sxs-lookup"><span data-stu-id="004fe-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-189">架構中參考的提供者沒有相對應的註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E \_ 不正確 \_ 提供者 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="004fe-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="004fe-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="004fe-192">架構中所參考的提供者的註冊不正確或不完整。</span><span class="sxs-lookup"><span data-stu-id="004fe-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="004fe-193">這項錯誤可能是由許多狀況所造成，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="004fe-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="004fe-194">在用來註冊提供者的受控物件格式 (MOF) 檔中遺漏[ \# pragma namespace](pragma-namespace.md)命令。</span><span class="sxs-lookup"><span data-stu-id="004fe-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="004fe-195">提供者可能會在錯誤的 WMI 命名空間中註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="004fe-196">無法取出 COM 註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="004fe-197">裝載模型無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-197">Hosting model is not valid.</span></span> <span data-ttu-id="004fe-198">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="004fe-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="004fe-199">註冊中指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="004fe-200">無法建立的實例或繼承自 [**\_ \_ Win32Provider**](--win32provider.md)類別，以便在 MOF 檔案中建立提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM \_ E \_ 提供者 \_ 載入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-202">2147749907 (0x80041013) </span><span class="sxs-lookup"><span data-stu-id="004fe-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-203">COM 無法找到結構描述中所參考的提供者。</span><span class="sxs-lookup"><span data-stu-id="004fe-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="004fe-204">這項錯誤可能是由許多狀況所造成，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="004fe-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="004fe-205">提供者使用的 WMI DLL 不符合建立提供者時所使用的 .lib 檔案。</span><span class="sxs-lookup"><span data-stu-id="004fe-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="004fe-206">提供者的 DLL 或其相依的任何 Dll 已損毀。</span><span class="sxs-lookup"><span data-stu-id="004fe-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="004fe-207">提供者無法匯出 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)。</span><span class="sxs-lookup"><span data-stu-id="004fe-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="004fe-208">未使用 **regsvr32** 命令註冊同進程提供者。</span><span class="sxs-lookup"><span data-stu-id="004fe-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="004fe-209">未使用 **/regserver** 參數註冊跨進程提供者。</span><span class="sxs-lookup"><span data-stu-id="004fe-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="004fe-210">例如， **myprog.exe/regserver**。</span><span class="sxs-lookup"><span data-stu-id="004fe-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-212">2147749908 (0x80041014) </span><span class="sxs-lookup"><span data-stu-id="004fe-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-213">元件（例如提供者）因內部原因而無法初始化。</span><span class="sxs-lookup"><span data-stu-id="004fe-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ E \_ 傳輸 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-215">2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="004fe-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-216">防止正常操作發生的網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ 不正確作業 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-218">2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="004fe-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-219">要求的作業無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-219">Requested operation is not valid.</span></span> <span data-ttu-id="004fe-220">這個錯誤通常發生於要刪除類別或屬性的無效嘗試。</span><span class="sxs-lookup"><span data-stu-id="004fe-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ 不正確 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="004fe-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-222">2147749911 (0x80041017) </span><span class="sxs-lookup"><span data-stu-id="004fe-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-223">查詢的語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM \_ E \_ 不正確 \_ 查詢 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-225">2147749912 (0x80041018) </span><span class="sxs-lookup"><span data-stu-id="004fe-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-226">不支援要求的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="004fe-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="004fe-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-228">2147749913 (0x80041019) </span><span class="sxs-lookup"><span data-stu-id="004fe-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-229">在 put 作業中，指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="004fe-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**\_ \_ \_ 不 \_ 允許使用 WBEM E 覆寫**</span><span class="sxs-lookup"><span data-stu-id="004fe-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-231">2147749914 (0x8004101A) </span><span class="sxs-lookup"><span data-stu-id="004fe-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-232">因為擁有物件不允許覆寫，所以無法對此限定詞執行加入作業。</span><span class="sxs-lookup"><span data-stu-id="004fe-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM \_ E 已 \_ 傳播 \_ 限定詞**</span><span class="sxs-lookup"><span data-stu-id="004fe-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-234">2147749915 (0x8004101B) </span><span class="sxs-lookup"><span data-stu-id="004fe-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-235">使用者嘗試刪除未擁有的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="004fe-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="004fe-236">限定詞繼承自父代類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM \_ E 已 \_ 傳播 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="004fe-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-238">2147749916 (0x8004101C) </span><span class="sxs-lookup"><span data-stu-id="004fe-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-239">使用者嘗試刪除未擁有的屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="004fe-240">屬性繼承自父代 (Parent) 類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E 未 \_ 預期**</span><span class="sxs-lookup"><span data-stu-id="004fe-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-242">2147749917 (0x8004101D) </span><span class="sxs-lookup"><span data-stu-id="004fe-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-243">用戶端進行了非預期和不合法的呼叫順序，例如在呼叫 [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)之前呼叫 [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) 。</span><span class="sxs-lookup"><span data-stu-id="004fe-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM \_ E 不 \_ 合法的 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="004fe-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-245">2147749918 (0x8004101E) </span><span class="sxs-lookup"><span data-stu-id="004fe-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-246">使用者要求了不合法的操作，例如從實例產生類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ 不 \_ 可以是索引 \_ 鍵**</span><span class="sxs-lookup"><span data-stu-id="004fe-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-248">2147749919 (0x8004101F) </span><span class="sxs-lookup"><span data-stu-id="004fe-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-249">在不能是索引鍵的屬性上指定索引鍵限定詞的行為不合法。</span><span class="sxs-lookup"><span data-stu-id="004fe-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="004fe-250">索引鍵會在物件的類別定義中指定，並且不能對每個執行個體進行變更。</span><span class="sxs-lookup"><span data-stu-id="004fe-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM \_ E \_ 未完成 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="004fe-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-252">2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="004fe-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-253">目前的物件不是有效的類別定義。</span><span class="sxs-lookup"><span data-stu-id="004fe-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="004fe-254">可能是未完成，或尚未使用 [**SWbemObject \_**](swbemobject-put-.md)向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ 不正確 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-256">2147749921 (0x80041021) </span><span class="sxs-lookup"><span data-stu-id="004fe-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-257">查詢的語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ NONDECORATED \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="004fe-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-259">2147749922 (0x80041022) </span><span class="sxs-lookup"><span data-stu-id="004fe-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-260">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ 唯讀 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-262">2147749923 (0x80041023) </span><span class="sxs-lookup"><span data-stu-id="004fe-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-263">已嘗試修改唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ 提供者 \_ 無法 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="004fe-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-265">2147749924 (0x80041024) </span><span class="sxs-lookup"><span data-stu-id="004fe-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-266">提供者無法執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="004fe-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="004fe-267">這可能包括太複雜的查詢、如何取出實例、建立或更新類別、刪除類別，或列舉類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E \_ 類別 \_ 具有 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="004fe-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-269">2147749925 (0x80041025) </span><span class="sxs-lookup"><span data-stu-id="004fe-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-270">嘗試進行變更，使子類別失效。</span><span class="sxs-lookup"><span data-stu-id="004fe-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ E \_ 類別 \_ 具有 \_ 實例**</span><span class="sxs-lookup"><span data-stu-id="004fe-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-272">2147749926 (0x80041026) </span><span class="sxs-lookup"><span data-stu-id="004fe-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-273">嘗試刪除或修改具有實例的類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_ \_ \_ 未執行 WBEM E \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="004fe-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-275">2147749927 (0x80041027) </span><span class="sxs-lookup"><span data-stu-id="004fe-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-276">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E 不 \_ 合法的 \_ Null**</span><span class="sxs-lookup"><span data-stu-id="004fe-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-278">2147749928 (0x80041028) </span><span class="sxs-lookup"><span data-stu-id="004fe-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-279">針對必須具有值的屬性指定了 Nothing/**Null** 值，例如由 [**索引**](optional-qualifiers.md)[**鍵**](key-qualifier.md)、索引或 **非 \_ Null** 限定詞標記的屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ 不正確辨識 \_ 符號 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-281">2147749929 (0x80041029) </span><span class="sxs-lookup"><span data-stu-id="004fe-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-282">提供的限定詞變數值不是合法的辨識符號類型。</span><span class="sxs-lookup"><span data-stu-id="004fe-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM \_ E \_ 不正確 \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-284">2147749930 (0x8004102A) </span><span class="sxs-lookup"><span data-stu-id="004fe-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-285">為屬性指定的 CIM 類型無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ 值 \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="004fe-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-287">2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="004fe-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-288">以超出範圍的值提出要求，或其與類型不相容。</span><span class="sxs-lookup"><span data-stu-id="004fe-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ 不 \_ 可以是 \_ 單一**</span><span class="sxs-lookup"><span data-stu-id="004fe-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-290">2147749932 (0x8004102C) </span><span class="sxs-lookup"><span data-stu-id="004fe-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-291">嘗試使類別成為 singleton，例如從非 singleton 類別衍生類別時。</span><span class="sxs-lookup"><span data-stu-id="004fe-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ 不正確 \_ CIM \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-293">2147749933 (0x8004102D) </span><span class="sxs-lookup"><span data-stu-id="004fe-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-294">指定的 CIM 類型無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ 無效 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="004fe-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-296">2147749934 (0x8004102E) </span><span class="sxs-lookup"><span data-stu-id="004fe-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-297">無法使用要求的方法。</span><span class="sxs-lookup"><span data-stu-id="004fe-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ 不正確 \_ 方法 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="004fe-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-299">2147749935 (0x8004102F) </span><span class="sxs-lookup"><span data-stu-id="004fe-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-300">為方法提供的參數無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ E \_ 系統 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="004fe-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-302">2147749936 (0x80041030) </span><span class="sxs-lookup"><span data-stu-id="004fe-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-303">嘗試取得系統屬性上的限定詞。</span><span class="sxs-lookup"><span data-stu-id="004fe-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM \_ E \_ 不正確 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="004fe-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-305">2147749937 (0x80041031) </span><span class="sxs-lookup"><span data-stu-id="004fe-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-306">無法辨識屬性類型。</span><span class="sxs-lookup"><span data-stu-id="004fe-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**已 \_ 取消 WBEM E \_ 通話 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-308">2147749938 (0x80041032) </span><span class="sxs-lookup"><span data-stu-id="004fe-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-309">非同步處理已在內部或由使用者取消。</span><span class="sxs-lookup"><span data-stu-id="004fe-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="004fe-310">請注意，由於非同步作業的時間和本質，此作業可能未真正取消。</span><span class="sxs-lookup"><span data-stu-id="004fe-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ 關機 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-312">2147749939 (0x80041033) </span><span class="sxs-lookup"><span data-stu-id="004fe-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-313">當 WMI 正在關機的過程中，使用者已要求操作。</span><span class="sxs-lookup"><span data-stu-id="004fe-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM \_ E \_ 傳播 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="004fe-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-315">2147749940 (0x80041034) </span><span class="sxs-lookup"><span data-stu-id="004fe-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-316">嘗試從父類別重複使用現有的方法名稱，但簽章不相符。</span><span class="sxs-lookup"><span data-stu-id="004fe-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM \_ E \_ 不支援的 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="004fe-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-318">2147749941 (0x80041035) </span><span class="sxs-lookup"><span data-stu-id="004fe-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-319">一個或多個參數值 (例如查詢文字) 過於複雜或不支援。</span><span class="sxs-lookup"><span data-stu-id="004fe-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="004fe-320">因此，會要求 WMI 以較簡單的參數重試此操作。</span><span class="sxs-lookup"><span data-stu-id="004fe-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ 缺少 \_ 參數 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="004fe-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-322">2147749942 (0x80041036) </span><span class="sxs-lookup"><span data-stu-id="004fe-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-323">方法呼叫中遺漏參數。</span><span class="sxs-lookup"><span data-stu-id="004fe-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM \_ E \_ 不正確 \_ 參數 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="004fe-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-325">2147749943 (0x80041037) </span><span class="sxs-lookup"><span data-stu-id="004fe-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-326">方法參數有不正確 [**識別碼**](standard-wmi-qualifiers.md) 限定詞。</span><span class="sxs-lookup"><span data-stu-id="004fe-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM \_ E 不 \_ 連續的 \_ 參數 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="004fe-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-328">2147749944 (0x80041038) </span><span class="sxs-lookup"><span data-stu-id="004fe-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-329">有一或多個方法參數的 [**識別碼**](standard-wmi-qualifiers.md) 限定詞不是順序。</span><span class="sxs-lookup"><span data-stu-id="004fe-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ \_ \_ RETVAL 上的 WBEM E 參數識別碼 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-331">2147749945 (0x80041039) </span><span class="sxs-lookup"><span data-stu-id="004fe-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-332">方法的傳回值具有 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="004fe-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ 不正確 \_ 物件 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="004fe-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-334">2147749946 (0x8004103A) </span><span class="sxs-lookup"><span data-stu-id="004fe-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-335">指定的物件路徑無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ \_ \_ 磁碟空間不足 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-337">2147749947 (0x8004103B) </span><span class="sxs-lookup"><span data-stu-id="004fe-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-338">磁碟空間不足，或已達到 (CIM 存放庫) 大小的 WMI 儲存機制的 4 GB 限制。</span><span class="sxs-lookup"><span data-stu-id="004fe-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM \_ E \_ 緩衝區 \_ 太 \_ 小**</span><span class="sxs-lookup"><span data-stu-id="004fe-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-340">2147749948 (0x8004103C) </span><span class="sxs-lookup"><span data-stu-id="004fe-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-341">提供的緩衝區太小，無法容納列舉值中的所有物件，或無法讀取字串屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E \_ 不支援的 \_ PUT \_ 延伸模組**</span><span class="sxs-lookup"><span data-stu-id="004fe-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-343">2147749949 (0x8004103D) </span><span class="sxs-lookup"><span data-stu-id="004fe-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-344">提供者不支援要求的 put 作業。</span><span class="sxs-lookup"><span data-stu-id="004fe-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ 未知的 \_ 物件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-346">2147749950 (0x8004103E) </span><span class="sxs-lookup"><span data-stu-id="004fe-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-347">封送處理期間遇到不正確類型或版本的物件。</span><span class="sxs-lookup"><span data-stu-id="004fe-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM \_ E \_ 未知的封 \_ 包 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-349">2147749951 (0x8004103F) </span><span class="sxs-lookup"><span data-stu-id="004fe-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-350">封送處理期間遇到不正確類型或版本的封包。</span><span class="sxs-lookup"><span data-stu-id="004fe-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM \_ E \_ 封送處理 \_ 版本 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="004fe-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-352">2147749952 (0x80041040) </span><span class="sxs-lookup"><span data-stu-id="004fe-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-353">封包有不支援的版本。</span><span class="sxs-lookup"><span data-stu-id="004fe-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ 封送處理 \_ 無效 \_ 的簽章**</span><span class="sxs-lookup"><span data-stu-id="004fe-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-355">2147749953 (0x80041041) </span><span class="sxs-lookup"><span data-stu-id="004fe-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-356">封包似乎已損毀。</span><span class="sxs-lookup"><span data-stu-id="004fe-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM \_ E \_ 不正確辨識 \_ 符號**</span><span class="sxs-lookup"><span data-stu-id="004fe-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-358">2147749954 (0x80041042) </span><span class="sxs-lookup"><span data-stu-id="004fe-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-359">嘗試不相符的限定詞，例如 \[ 在物件上放置索引鍵， \] 而不是在屬性上進行。</span><span class="sxs-lookup"><span data-stu-id="004fe-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E \_ 不正確 \_ 重複 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="004fe-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-361">2147749955 (0x80041043) </span><span class="sxs-lookup"><span data-stu-id="004fe-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-362">在 CIM 方法中宣告了重複的參數。</span><span class="sxs-lookup"><span data-stu-id="004fe-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ 電子 \_ \_ 資料太多 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-364">2147749956 (0x80041044) </span><span class="sxs-lookup"><span data-stu-id="004fe-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-365">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ SERVER \_ 太 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="004fe-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-367">2147749957 (0x80041045) </span><span class="sxs-lookup"><span data-stu-id="004fe-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-368">[**IWbemObjectSink：：表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="004fe-369">提供者可以 refire 事件。</span><span class="sxs-lookup"><span data-stu-id="004fe-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E \_ 不正確類別 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-371">2147749958 (0x80041046) </span><span class="sxs-lookup"><span data-stu-id="004fe-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-372">指定的限定詞類別無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM \_ E \_ 迴圈 \_ 參考**</span><span class="sxs-lookup"><span data-stu-id="004fe-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-374">2147749959 (0x80041047) </span><span class="sxs-lookup"><span data-stu-id="004fe-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-375">嘗試建立迴圈 (的參考，例如，衍生類別本身) 。</span><span class="sxs-lookup"><span data-stu-id="004fe-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ 不支援的 \_ 類別 \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="004fe-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-377">2147749960 (0x80041048) </span><span class="sxs-lookup"><span data-stu-id="004fe-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-378">不支援指定的類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ 無法 \_ 變更 \_ 金鑰 \_ 繼承**</span><span class="sxs-lookup"><span data-stu-id="004fe-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-380">2147749961 (0x80041049) </span><span class="sxs-lookup"><span data-stu-id="004fe-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-381">嘗試在實例或子類別已使用金鑰時變更金鑰。</span><span class="sxs-lookup"><span data-stu-id="004fe-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ 無法 \_ 變更 \_ 索引 \_ 繼承**</span><span class="sxs-lookup"><span data-stu-id="004fe-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-383">2147749968 (0x80041050) </span><span class="sxs-lookup"><span data-stu-id="004fe-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-384">當實例或子類別已經在使用索引時，嘗試變更索引。</span><span class="sxs-lookup"><span data-stu-id="004fe-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ 的 \_ 屬性太多 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-386">2147749969 (0x80041051) </span><span class="sxs-lookup"><span data-stu-id="004fe-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-387">嘗試建立的屬性多於目前版本類別所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ 更新 \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="004fe-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-389">2147749970 (0x80041052) </span><span class="sxs-lookup"><span data-stu-id="004fe-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-390">在衍生類別中重新定義了具有衝突類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_ \_ \_ \_ 不 \_ 允許使用 WBEM E 更新覆寫**</span><span class="sxs-lookup"><span data-stu-id="004fe-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-392">2147749971 (0x80041053) </span><span class="sxs-lookup"><span data-stu-id="004fe-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-393">嘗試在衍生類別中進行覆寫無法覆寫的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="004fe-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM \_ E \_ 更新 \_ 傳播 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="004fe-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-395">2147749972 (0x80041054) </span><span class="sxs-lookup"><span data-stu-id="004fe-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-396">已使用衍生類別中的衝突簽章重新宣告方法。</span><span class="sxs-lookup"><span data-stu-id="004fe-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM \_ E \_ 方法 \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="004fe-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-398">2147749973 (0x80041055) </span><span class="sxs-lookup"><span data-stu-id="004fe-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-399">嘗試執行未標示為 \[ \] 在任何相關類別中執行的方法。</span><span class="sxs-lookup"><span data-stu-id="004fe-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="004fe-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="004fe-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="004fe-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="004fe-402">嘗試執行標示為停用的方法 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="004fe-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E \_ 複習複習 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="004fe-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-404">2147749975 (0x80041057) </span><span class="sxs-lookup"><span data-stu-id="004fe-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-405">重新整理程式正忙於其他作業。</span><span class="sxs-lookup"><span data-stu-id="004fe-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM E 無法剖析的 \_ \_ \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="004fe-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-407">2147749976 (0x80041058) </span><span class="sxs-lookup"><span data-stu-id="004fe-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-408">篩選查詢的語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ NOT \_ 事件 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="004fe-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-410">2147749977 (0x80041059) </span><span class="sxs-lookup"><span data-stu-id="004fe-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-411">篩選查詢的 FROM 子句參考的類別不是事件類別， (並非衍生自 [**\_ \_ 事件**](--event.md)) 。</span><span class="sxs-lookup"><span data-stu-id="004fe-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ 遺失 \_ 群組 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-413">2147749978 (0x8004105A) </span><span class="sxs-lookup"><span data-stu-id="004fe-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-414">使用 GROUP BY 子句，而不使用對應的 GROUP WITHIN 子句。</span><span class="sxs-lookup"><span data-stu-id="004fe-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ 遺失 \_ 匯總 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="004fe-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-416">2147749979 (0x8004105B) </span><span class="sxs-lookup"><span data-stu-id="004fe-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-417">使用 GROUP BY 子句。</span><span class="sxs-lookup"><span data-stu-id="004fe-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="004fe-418">不支援所有屬性的彙總 (Aggregation)。</span><span class="sxs-lookup"><span data-stu-id="004fe-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ E \_ 屬性 \_ 不 \_ 是 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="004fe-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-420">2147749980 (0x8004105C) </span><span class="sxs-lookup"><span data-stu-id="004fe-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-421">點標記法使用於不是內嵌物件的屬性上。</span><span class="sxs-lookup"><span data-stu-id="004fe-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ \_ 以物件匯總的 WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-423">2147749981 (0x8004105D) </span><span class="sxs-lookup"><span data-stu-id="004fe-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-424">GROUP BY 子句不使用點標記法參考做為內嵌物件 (Embedded Object) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="004fe-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM \_ E \_ UNINTERPRETABLE \_ 提供者 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="004fe-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-426">2147749983 (0x8004105F) </span><span class="sxs-lookup"><span data-stu-id="004fe-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-427">事件提供者註冊查詢 ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) 未指定提供事件的類別。</span><span class="sxs-lookup"><span data-stu-id="004fe-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ 備份 \_ 還原 \_ WINMGMT \_ 正在執行**</span><span class="sxs-lookup"><span data-stu-id="004fe-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-429">2147749984 (0x80041060) </span><span class="sxs-lookup"><span data-stu-id="004fe-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-430">要求在 WinMgmt.exe 或包含 WMI 服務的 SVCHOST 進程使用時，備份或還原存放庫。</span><span class="sxs-lookup"><span data-stu-id="004fe-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM \_ E \_ 佇列 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="004fe-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-432">2147749985 (0x80041061) </span><span class="sxs-lookup"><span data-stu-id="004fe-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-433">事件取用者的非同步傳遞佇列溢位太慢。</span><span class="sxs-lookup"><span data-stu-id="004fe-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_ \_ \_ 未保留 WBEM E \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="004fe-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-435">2147749986 (0x80041062) </span><span class="sxs-lookup"><span data-stu-id="004fe-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-436">因為用戶端沒有必要的安全性許可權，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ 無效 \_ 運算子**</span><span class="sxs-lookup"><span data-stu-id="004fe-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-438">2147749987 (0x80041063) </span><span class="sxs-lookup"><span data-stu-id="004fe-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-439">運算子對此屬性類型無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM \_ E \_ 本機 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="004fe-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-441">2147749988 (0x80041064) </span><span class="sxs-lookup"><span data-stu-id="004fe-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-442">使用者在本機連接上指定了使用者名稱/密碼/授權單位。</span><span class="sxs-lookup"><span data-stu-id="004fe-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="004fe-443">使用者必須使用空白的使用者名稱/密碼，並且依賴預設安全性。</span><span class="sxs-lookup"><span data-stu-id="004fe-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ 不 \_ 可以是 \_ 抽象的**</span><span class="sxs-lookup"><span data-stu-id="004fe-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-445">2147749989 (0x80041065) </span><span class="sxs-lookup"><span data-stu-id="004fe-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-446">類別在其父類別不是抽象時成為抽象。</span><span class="sxs-lookup"><span data-stu-id="004fe-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ 修改過的 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="004fe-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-448">2147749990 (0x80041066) </span><span class="sxs-lookup"><span data-stu-id="004fe-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-449">未使用 WBEM 旗標來寫入修改過的物件， **\_ 請使用指定的 \_ \_ 修改 \_ 限定詞** 旗標。</span><span class="sxs-lookup"><span data-stu-id="004fe-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM \_ E \_ 用戶端 \_ 太 \_ 慢**</span><span class="sxs-lookup"><span data-stu-id="004fe-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-451">2147749991 (0x80041067) </span><span class="sxs-lookup"><span data-stu-id="004fe-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-452">用戶端無法從列舉快速地取出物件。</span><span class="sxs-lookup"><span data-stu-id="004fe-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="004fe-453">當用戶端建立列舉物件時，會傳回此常數，但不會及時從列舉值抓取物件，進而導致列舉值的物件快取進行備份。</span><span class="sxs-lookup"><span data-stu-id="004fe-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ Null \_ 安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="004fe-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-455">2147749992 (0x80041068) </span><span class="sxs-lookup"><span data-stu-id="004fe-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-456">已使用 Null 安全描述項。</span><span class="sxs-lookup"><span data-stu-id="004fe-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-458">2147749993 (0x80041069) </span><span class="sxs-lookup"><span data-stu-id="004fe-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-459">作業超時。</span><span class="sxs-lookup"><span data-stu-id="004fe-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ 不正確 \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="004fe-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="004fe-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="004fe-462">關聯無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM \_ E 不 \_ 明確的 \_ 運算**</span><span class="sxs-lookup"><span data-stu-id="004fe-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-464">2147749995 (0x8004106B) </span><span class="sxs-lookup"><span data-stu-id="004fe-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-465">運算不明確。</span><span class="sxs-lookup"><span data-stu-id="004fe-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM \_ E \_ 配額 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="004fe-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-467">2147749996 (0x8004106C) </span><span class="sxs-lookup"><span data-stu-id="004fe-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-468">WMI 佔用太多記憶體。</span><span class="sxs-lookup"><span data-stu-id="004fe-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="004fe-469">這可能是因為記憶體可用性不足或 WMI 耗用過多記憶體所致。</span><span class="sxs-lookup"><span data-stu-id="004fe-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E \_ 交易 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="004fe-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-471">2147749997 (0x8004106D) </span><span class="sxs-lookup"><span data-stu-id="004fe-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-472">作業導致交易衝突。</span><span class="sxs-lookup"><span data-stu-id="004fe-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM \_ E \_ 強制 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="004fe-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-474">2147749998 (0x8004106E) </span><span class="sxs-lookup"><span data-stu-id="004fe-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-475">交易強制執行回復。</span><span class="sxs-lookup"><span data-stu-id="004fe-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E \_ 不支援的 \_ 地區設定**</span><span class="sxs-lookup"><span data-stu-id="004fe-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-477">2147749999 (0x8004106F) </span><span class="sxs-lookup"><span data-stu-id="004fe-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-478">不支援在呼叫中使用的地區設定。</span><span class="sxs-lookup"><span data-stu-id="004fe-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ 句 \_ 柄 \_ 過期 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-480">2147750000 (0x80041070) </span><span class="sxs-lookup"><span data-stu-id="004fe-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-481">物件控制碼已過期。</span><span class="sxs-lookup"><span data-stu-id="004fe-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM \_ E \_ 連接 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="004fe-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-483">2147750001 (0x80041071) </span><span class="sxs-lookup"><span data-stu-id="004fe-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-484">連接至 SQL 資料庫失敗。</span><span class="sxs-lookup"><span data-stu-id="004fe-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E \_ 不正確 \_ 控制碼 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="004fe-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-486">2147750002 (0x80041072) </span><span class="sxs-lookup"><span data-stu-id="004fe-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-487">控制碼要求無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM \_ E \_ 屬性 \_ 名稱 \_ 太 \_ 寬**</span><span class="sxs-lookup"><span data-stu-id="004fe-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-489">2147750003 (0x80041073) </span><span class="sxs-lookup"><span data-stu-id="004fe-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-490">屬性名稱包含超過255個字元。</span><span class="sxs-lookup"><span data-stu-id="004fe-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ E \_ 類別 \_ 名稱 \_ 太 \_ 寬**</span><span class="sxs-lookup"><span data-stu-id="004fe-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-492">2147750004 (0x80041074) </span><span class="sxs-lookup"><span data-stu-id="004fe-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-493">類別名稱包含超過255個字元。</span><span class="sxs-lookup"><span data-stu-id="004fe-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM \_ E \_ 方法 \_ 名稱 \_ 太 \_ 寬**</span><span class="sxs-lookup"><span data-stu-id="004fe-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-495">2147750005 (0x80041075) </span><span class="sxs-lookup"><span data-stu-id="004fe-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-496">方法名稱包含超過255個字元。</span><span class="sxs-lookup"><span data-stu-id="004fe-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM \_ E 辨識 \_ 符號 \_ 名稱 \_ 太 \_ 寬**</span><span class="sxs-lookup"><span data-stu-id="004fe-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-498">2147750006 (0x80041076) </span><span class="sxs-lookup"><span data-stu-id="004fe-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-499">限定詞名稱包含超過255個字元。</span><span class="sxs-lookup"><span data-stu-id="004fe-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM \_ E \_ 重新執行 \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="004fe-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-501">2147750007 (0x80041077) </span><span class="sxs-lookup"><span data-stu-id="004fe-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-502">因為 SQL 中有鎖死，所以必須重新執行 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="004fe-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="004fe-503">只有當資料儲存在 SQL 資料庫中時，才會傳回此項。</span><span class="sxs-lookup"><span data-stu-id="004fe-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E \_ 資料庫 \_ VER \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="004fe-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-505">2147750008 (0x80041078) </span><span class="sxs-lookup"><span data-stu-id="004fe-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-506">資料庫版本與存放庫驅動程式所處理的版本不相符。</span><span class="sxs-lookup"><span data-stu-id="004fe-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ 拒絕 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="004fe-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-508">2147750009 (0x80041079) </span><span class="sxs-lookup"><span data-stu-id="004fe-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-509">WMI 無法執行刪除作業，因為提供者不允許該操作。</span><span class="sxs-lookup"><span data-stu-id="004fe-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ 否決 \_ PUT**</span><span class="sxs-lookup"><span data-stu-id="004fe-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-511">2147750010 (0x8004107A) </span><span class="sxs-lookup"><span data-stu-id="004fe-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-512">WMI 無法執行 put 作業，因為提供者不允許此操作。</span><span class="sxs-lookup"><span data-stu-id="004fe-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E \_ 不正確 \_ 地區設定**</span><span class="sxs-lookup"><span data-stu-id="004fe-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-514">2147750016 (0x80041080) </span><span class="sxs-lookup"><span data-stu-id="004fe-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-515">指定的地區設定識別碼對作業無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**已 \_ 暫停 WBEM E \_ 提供者 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-517">2147750017 (0x80041081) </span><span class="sxs-lookup"><span data-stu-id="004fe-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-518">提供者已暫止。</span><span class="sxs-lookup"><span data-stu-id="004fe-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_需要 WBEM E \_ 同步 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="004fe-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-520">2147750018 (0x80041082) </span><span class="sxs-lookup"><span data-stu-id="004fe-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-521">物件必須寫入至 WMI 儲存機制，並再次抓取，要求的作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="004fe-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="004fe-522">當必須認可並抓取物件以查看屬性值時，就會傳回這個常數。</span><span class="sxs-lookup"><span data-stu-id="004fe-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ 沒有 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="004fe-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-524">2147750019 (0x80041083) </span><span class="sxs-lookup"><span data-stu-id="004fe-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-525">無法完成操作;沒有任何可用的架構。</span><span class="sxs-lookup"><span data-stu-id="004fe-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_ \_ \_ 已註冊 WBEM E 提供者 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-527">02147750020 (0x119FD010) </span><span class="sxs-lookup"><span data-stu-id="004fe-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-528">因為提供者已經註冊，所以無法註冊。</span><span class="sxs-lookup"><span data-stu-id="004fe-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E \_ 提供者 \_ 未 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="004fe-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-530">2147750021 (0x80041085) </span><span class="sxs-lookup"><span data-stu-id="004fe-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-531">未註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="004fe-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM \_ E \_ 嚴重 \_ 傳輸 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="004fe-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-533">2147750022 (0x80041086) </span><span class="sxs-lookup"><span data-stu-id="004fe-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-534">發生嚴重的傳輸錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_需要 WBEM E \_ 加密 \_ 連接 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-536">2147750023 (0x80041087) </span><span class="sxs-lookup"><span data-stu-id="004fe-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-537">使用者嘗試設定沒有加密連接的電腦名稱稱或網域。</span><span class="sxs-lookup"><span data-stu-id="004fe-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM \_ E \_ 提供者已 \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-539">2147750024 (0x80041088) </span><span class="sxs-lookup"><span data-stu-id="004fe-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-540">提供者無法在指定的超時時間內報告結果。</span><span class="sxs-lookup"><span data-stu-id="004fe-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ 無 \_ 按鍵**</span><span class="sxs-lookup"><span data-stu-id="004fe-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-542">2147750025 (0x80041089) </span><span class="sxs-lookup"><span data-stu-id="004fe-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-543">使用者嘗試放置未定義索引鍵的實例。</span><span class="sxs-lookup"><span data-stu-id="004fe-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_ \_ 已停用 WBEM E 提供者 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-545">2147750026 (0x8004108A) </span><span class="sxs-lookup"><span data-stu-id="004fe-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-546">使用者嘗試註冊提供者實例，但已卸載提供者實例的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="004fe-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ E \_ 註冊 \_ 太 \_ 廣泛**</span><span class="sxs-lookup"><span data-stu-id="004fe-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-548">2147753985 (0x80042001) </span><span class="sxs-lookup"><span data-stu-id="004fe-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-549">提供者註冊與系統事件網域重迭。</span><span class="sxs-lookup"><span data-stu-id="004fe-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ 註冊 \_ 太 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="004fe-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-551">2147753986 (0x80042002) </span><span class="sxs-lookup"><span data-stu-id="004fe-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-552">這個查詢中未使用 WITHIN 子句。</span><span class="sxs-lookup"><span data-stu-id="004fe-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ 授權 \_ 不具特殊 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="004fe-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-554">2147753987 (0x80042003) </span><span class="sxs-lookup"><span data-stu-id="004fe-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-555">這部電腦沒有必要的網域許可權，無法支援與所建立訂用帳戶實例相關的安全性功能。</span><span class="sxs-lookup"><span data-stu-id="004fe-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="004fe-556">請聯絡網域系統管理員，將此電腦新增至 Windows 授權存取群組。</span><span class="sxs-lookup"><span data-stu-id="004fe-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ 稍後重試 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-558">2147758081 (0x80043001) </span><span class="sxs-lookup"><span data-stu-id="004fe-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-559">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM \_ E \_ 資源 \_ 爭用**</span><span class="sxs-lookup"><span data-stu-id="004fe-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-561">2147758082 (0x80043002) </span><span class="sxs-lookup"><span data-stu-id="004fe-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-562">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ 電子 \_ 預期的辨識 \_ 符號 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="004fe-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-564">2147762177 (0x80044001) </span><span class="sxs-lookup"><span data-stu-id="004fe-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-565">必須是辨識符號名稱。</span><span class="sxs-lookup"><span data-stu-id="004fe-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E 必須 \_ 為 \_ 半**</span><span class="sxs-lookup"><span data-stu-id="004fe-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-567">2147762178 (0x80044002) </span><span class="sxs-lookup"><span data-stu-id="004fe-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-568">必須是分號或 ' = '。</span><span class="sxs-lookup"><span data-stu-id="004fe-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 左 \_ 大括弧**</span><span class="sxs-lookup"><span data-stu-id="004fe-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-570">2147762179 (0x80044003) </span><span class="sxs-lookup"><span data-stu-id="004fe-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-571">需要左大括弧。</span><span class="sxs-lookup"><span data-stu-id="004fe-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ 應有 \_ 右 \_ 大括弧**</span><span class="sxs-lookup"><span data-stu-id="004fe-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-573">2147762180 (0x80044004) </span><span class="sxs-lookup"><span data-stu-id="004fe-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-574">遺漏右大括弧或不合法的陣列元素。</span><span class="sxs-lookup"><span data-stu-id="004fe-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ 應有 \_ 右 \_ 括弧**</span><span class="sxs-lookup"><span data-stu-id="004fe-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-576">2147762181 (0x80044005) </span><span class="sxs-lookup"><span data-stu-id="004fe-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-577">必須是右括弧。</span><span class="sxs-lookup"><span data-stu-id="004fe-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ 預期 \_ 右 \_ 括弧**</span><span class="sxs-lookup"><span data-stu-id="004fe-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-579">2147762182 (0x80044006) </span><span class="sxs-lookup"><span data-stu-id="004fe-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-580">需要右括弧。</span><span class="sxs-lookup"><span data-stu-id="004fe-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E 不 \_ 合法的 \_ 常 \_ 數值**</span><span class="sxs-lookup"><span data-stu-id="004fe-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-582">2147762183 (0x80044007) </span><span class="sxs-lookup"><span data-stu-id="004fe-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-583">數值超出範圍或不含引號的字串。</span><span class="sxs-lookup"><span data-stu-id="004fe-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ 預期的 \_ 類型 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="004fe-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-585">2147762184 (0x80044008) </span><span class="sxs-lookup"><span data-stu-id="004fe-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-586">必須是類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 左 \_ 括弧**</span><span class="sxs-lookup"><span data-stu-id="004fe-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-588">2147762185 (0x80044009) </span><span class="sxs-lookup"><span data-stu-id="004fe-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-589">應為左括弧。</span><span class="sxs-lookup"><span data-stu-id="004fe-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ 無法辨識的 \_ 權杖**</span><span class="sxs-lookup"><span data-stu-id="004fe-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-591">2147762186 (0x8004400A) </span><span class="sxs-lookup"><span data-stu-id="004fe-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-592">檔案中有未預期的標記。</span><span class="sxs-lookup"><span data-stu-id="004fe-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ 無法辨識的 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-594">2147762187 (0x8004400B) </span><span class="sxs-lookup"><span data-stu-id="004fe-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-595">無法辨識或不支援的類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ 預期的 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="004fe-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-597">2147762187 (0x8004400B) </span><span class="sxs-lookup"><span data-stu-id="004fe-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-598">預期的屬性或方法名稱。</span><span class="sxs-lookup"><span data-stu-id="004fe-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**\_ \_ \_ 不支援 WBEMMOF E \_ TYPEDEF**</span><span class="sxs-lookup"><span data-stu-id="004fe-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-600">2147762189 (0x8004400D) </span><span class="sxs-lookup"><span data-stu-id="004fe-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-601">不支援 typedef 和列舉類型。</span><span class="sxs-lookup"><span data-stu-id="004fe-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E 未 \_ 預期的 \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="004fe-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-603">2147762190 (0x8004400E) </span><span class="sxs-lookup"><span data-stu-id="004fe-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-604">只有類別物件的參考可以有別名值。</span><span class="sxs-lookup"><span data-stu-id="004fe-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E 未 \_ 預期的 \_ 陣列 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="004fe-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-606">2147762191 (0x8004400F) </span><span class="sxs-lookup"><span data-stu-id="004fe-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-607">未預期的陣列初始化。</span><span class="sxs-lookup"><span data-stu-id="004fe-607">Unexpected array initialization.</span></span> <span data-ttu-id="004fe-608">陣列必須使用宣告 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="004fe-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 修訂 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-610">2147762192 (0x80044010) </span><span class="sxs-lookup"><span data-stu-id="004fe-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-611">命名空間路徑語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ 電子 \_ \_ 重複 \_ 修訂無效**</span><span class="sxs-lookup"><span data-stu-id="004fe-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-613">2147762193 (0x80044011) </span><span class="sxs-lookup"><span data-stu-id="004fe-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-614">重複的修訂規範。</span><span class="sxs-lookup"><span data-stu-id="004fe-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ 不正確 \_ PRAGMA**</span><span class="sxs-lookup"><span data-stu-id="004fe-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-616">2147762194 (0x80044012) </span><span class="sxs-lookup"><span data-stu-id="004fe-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-617">[ \# pragma](pragma-namespace.md)之後必須接著有效的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="004fe-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 命名空間 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-619">2147762195 (0x80044013) </span><span class="sxs-lookup"><span data-stu-id="004fe-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-620">命名空間路徑語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ 需要的 \_ 類別 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="004fe-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-622">2147762196 (0x80044014) </span><span class="sxs-lookup"><span data-stu-id="004fe-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-623">類別名稱中未預期的字元必須是識別碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF \_ E \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="004fe-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-625">2147762197 (0x80044015) </span><span class="sxs-lookup"><span data-stu-id="004fe-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-626">指定的值不能成為適當的類型。</span><span class="sxs-lookup"><span data-stu-id="004fe-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 別名 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="004fe-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-628">2147762198 (0x80044016) </span><span class="sxs-lookup"><span data-stu-id="004fe-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-629">貨幣符號後面必須接著別名名稱作為識別碼。</span><span class="sxs-lookup"><span data-stu-id="004fe-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ 不正確 \_ 類別 \_ 宣告**</span><span class="sxs-lookup"><span data-stu-id="004fe-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-631">2147762199 (0x80044017) </span><span class="sxs-lookup"><span data-stu-id="004fe-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-632">類別宣告無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ 不正確 \_ 實例 \_ 宣告**</span><span class="sxs-lookup"><span data-stu-id="004fe-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-634">2147762200 (0x80044018) </span><span class="sxs-lookup"><span data-stu-id="004fe-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-635">實例宣告無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-635">The instance declaration is not valid.</span></span> <span data-ttu-id="004fe-636">它必須以 "instance of" 開頭</span><span class="sxs-lookup"><span data-stu-id="004fe-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ 電子 \_ 預期的 \_ 貨幣**</span><span class="sxs-lookup"><span data-stu-id="004fe-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-638">2147762201 (0x80044019) </span><span class="sxs-lookup"><span data-stu-id="004fe-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-639">預期的貨幣符號。</span><span class="sxs-lookup"><span data-stu-id="004fe-639">Expected dollar sign.</span></span> <span data-ttu-id="004fe-640">格式為 "$name" 的別名必須遵照 "as" 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="004fe-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF \_ E \_ CIMTYPE 辨識 \_ 符號**</span><span class="sxs-lookup"><span data-stu-id="004fe-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-642">2147762202 (0x8004401A) </span><span class="sxs-lookup"><span data-stu-id="004fe-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-643">無法直接在 MOF 檔案中指定 "CIMTYPE" 限定詞。</span><span class="sxs-lookup"><span data-stu-id="004fe-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="004fe-644">使用標準類型標記法。</span><span class="sxs-lookup"><span data-stu-id="004fe-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ 重複 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="004fe-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-646">2147762203 (0x8004401B) </span><span class="sxs-lookup"><span data-stu-id="004fe-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-647">MOF 中找到重複的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="004fe-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ 不正確 \_ 命名空間 \_ 規格**</span><span class="sxs-lookup"><span data-stu-id="004fe-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-649">2147762204 (0x8004401C) </span><span class="sxs-lookup"><span data-stu-id="004fe-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-650">命名空間語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="004fe-651">不允許對其他伺服器的參考。</span><span class="sxs-lookup"><span data-stu-id="004fe-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="004fe-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-653">2147762205 (0x8004401D) </span><span class="sxs-lookup"><span data-stu-id="004fe-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-654">值超出範圍。</span><span class="sxs-lookup"><span data-stu-id="004fe-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ 電子 \_ 不正確檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-656">2147762206 (0x8004401E) </span><span class="sxs-lookup"><span data-stu-id="004fe-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-657">檔案不是有效的文字 MOF 檔案或二進位 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="004fe-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ \_ \_ EMBEDDED 中的 E 別名 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-659">2147762207 (0x8004401F) </span><span class="sxs-lookup"><span data-stu-id="004fe-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-660">内嵌物件不可以是別名。</span><span class="sxs-lookup"><span data-stu-id="004fe-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ Null \_ 陣列 \_ ELEM**</span><span class="sxs-lookup"><span data-stu-id="004fe-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-662">2147762208 (0x80044020) </span><span class="sxs-lookup"><span data-stu-id="004fe-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-663">陣列中的 Null 元素不受支援。</span><span class="sxs-lookup"><span data-stu-id="004fe-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF \_ E \_ 重複辨識 \_ 符號**</span><span class="sxs-lookup"><span data-stu-id="004fe-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-665">2147762209 (0x80044021) </span><span class="sxs-lookup"><span data-stu-id="004fe-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-666">物件上的限定詞使用了一次以上。</span><span class="sxs-lookup"><span data-stu-id="004fe-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ 預期 \_ 的 \_ 類型類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-668">2147762210 (0x80044022) </span><span class="sxs-lookup"><span data-stu-id="004fe-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-669">必須是類別類型，例如 **ToInstance**、 **ToSubClass**、 **EnableOverride** 或 **DisableOverride**。</span><span class="sxs-lookup"><span data-stu-id="004fe-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF \_ E \_ 不相容的 \_ \_ 種類類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-671">2147762211 (0x80044023) </span><span class="sxs-lookup"><span data-stu-id="004fe-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-672">在相同的辨識符號上結合 **EnableOverride** 和 **DisableOverride** 並不合法。</span><span class="sxs-lookup"><span data-stu-id="004fe-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ 多個 \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="004fe-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-674">2147762212 (0x80044024) </span><span class="sxs-lookup"><span data-stu-id="004fe-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-675">別名不可使用兩次。</span><span class="sxs-lookup"><span data-stu-id="004fe-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ 不相容的類別 \_ \_ TYPES2**</span><span class="sxs-lookup"><span data-stu-id="004fe-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-677">2147762213 (0x80044025) </span><span class="sxs-lookup"><span data-stu-id="004fe-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-678">組合 **受限** 的、 **ToInstance** 或 **ToSubClass** 並不合法。</span><span class="sxs-lookup"><span data-stu-id="004fe-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ 未 \_ \_ 傳回陣列**</span><span class="sxs-lookup"><span data-stu-id="004fe-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-680">2147762214 (0x80044026) </span><span class="sxs-lookup"><span data-stu-id="004fe-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-681">方法無法傳回陣列值。</span><span class="sxs-lookup"><span data-stu-id="004fe-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ 必須 \_ 是 \_ IN \_ 或 \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="004fe-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-683">2147762215 (0x80044027) </span><span class="sxs-lookup"><span data-stu-id="004fe-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-684">引數必須有 **In** 或 **Out** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="004fe-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ 旗標 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-686">2147762216 (0x80044028) </span><span class="sxs-lookup"><span data-stu-id="004fe-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-687">旗標語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E 必須是 \_ \_ 大括弧 \_ 或不 \_ 正確的 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-689">2147762217 (0x80044029) </span><span class="sxs-lookup"><span data-stu-id="004fe-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-690">遺漏了類別的最後大括弧和分號。</span><span class="sxs-lookup"><span data-stu-id="004fe-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ 不支援的 \_ CIMV22 \_ QUAL \_ 值**</span><span class="sxs-lookup"><span data-stu-id="004fe-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-692">2147762218 (0x8004402A) </span><span class="sxs-lookup"><span data-stu-id="004fe-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-693">限定詞值不支援 CIM 2.2 版的功能。</span><span class="sxs-lookup"><span data-stu-id="004fe-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ 不支援的 \_ CIMV22 \_ 資料 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="004fe-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-695">2147762219 (0x8004402B) </span><span class="sxs-lookup"><span data-stu-id="004fe-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-696">不支援 CIM 版本2.2 資料類型。</span><span class="sxs-lookup"><span data-stu-id="004fe-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ DELETEINSTANCE \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-698">2147762220 (0x8004402C) </span><span class="sxs-lookup"><span data-stu-id="004fe-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-699">刪除實例語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="004fe-700">它應該是 `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="004fe-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ 不正確辨識 \_ 符號 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-702">2147762221 (0x8004402D) </span><span class="sxs-lookup"><span data-stu-id="004fe-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-703">限定詞語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="004fe-704">此屬性應該是 `qualifiername:type=value,scope(class|instance), flavorname`。</span><span class="sxs-lookup"><span data-stu-id="004fe-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ \_ \_ 範圍外使用的 WBEMMOF E 限定詞 \_**</span><span class="sxs-lookup"><span data-stu-id="004fe-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-706">2147762222 (0x8004402E) </span><span class="sxs-lookup"><span data-stu-id="004fe-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-707">限定詞會在其範圍之外使用。</span><span class="sxs-lookup"><span data-stu-id="004fe-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**\_ \_ \_ 建立 \_ 臨時 \_ 檔時發生 WBEMMOF E 錯誤**</span><span class="sxs-lookup"><span data-stu-id="004fe-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-709">2147762223 (0x8004402F) </span><span class="sxs-lookup"><span data-stu-id="004fe-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-710">建立暫存檔案時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="004fe-710">Error creating temporary file.</span></span> <span data-ttu-id="004fe-711">暫存檔案是 MOF 編譯中的中繼階段。</span><span class="sxs-lookup"><span data-stu-id="004fe-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ ERROR \_ 不正確 \_ INCLUDE \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="004fe-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-713">2147762224 (0x80044030) </span><span class="sxs-lookup"><span data-stu-id="004fe-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-714">預處理器命令[ \# 包含](-include.md)MOF 中包含的檔案無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="004fe-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ 不正確 \_ DELETECLASS \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="004fe-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="004fe-716">2147762225 (0x80044031) </span><span class="sxs-lookup"><span data-stu-id="004fe-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="004fe-717">預處理器命令[ \# pragma deleteinstance](pragma-deleteinstance.md)或[ \# pragma deleteclass](pragma-deleteclass.md)的語法無效。</span><span class="sxs-lookup"><span data-stu-id="004fe-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="004fe-718">規格需求</span><span class="sxs-lookup"><span data-stu-id="004fe-718">Requirements</span></span>



| <span data-ttu-id="004fe-719">需求</span><span class="sxs-lookup"><span data-stu-id="004fe-719">Requirement</span></span> | <span data-ttu-id="004fe-720">值</span><span class="sxs-lookup"><span data-stu-id="004fe-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="004fe-721">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="004fe-721">Minimum supported client</span></span><br/> | <span data-ttu-id="004fe-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="004fe-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="004fe-723">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="004fe-723">Minimum supported server</span></span><br/> | <span data-ttu-id="004fe-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="004fe-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="004fe-725">標頭</span><span class="sxs-lookup"><span data-stu-id="004fe-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="004fe-726"><dt>WbemCli。h</dt></span><span class="sxs-lookup"><span data-stu-id="004fe-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="004fe-727">Idl</span><span class="sxs-lookup"><span data-stu-id="004fe-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="004fe-728"><dt>WbemCli .idl</dt></span><span class="sxs-lookup"><span data-stu-id="004fe-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004fe-729">另請參閱</span><span class="sxs-lookup"><span data-stu-id="004fe-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004fe-730">WMI 傳回碼</span><span class="sxs-lookup"><span data-stu-id="004fe-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

