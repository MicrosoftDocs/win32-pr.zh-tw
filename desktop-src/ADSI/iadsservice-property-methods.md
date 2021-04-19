---
title: 'IADsService 屬性方法 (Iads .h) '
description: 讀取及寫入本主題中所述的屬性。
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- IADsService 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969579"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="b69a2-104">IADsService 屬性方法</span><span class="sxs-lookup"><span data-stu-id="b69a2-104">IADsService Property Methods</span></span>

<span data-ttu-id="b69a2-105">[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)介面的屬性方法會讀取及寫入本主題中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="b69a2-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="b69a2-106">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="b69a2-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b69a2-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b69a2-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b69a2-108">**Dependencies** (相依性)</span><span class="sxs-lookup"><span data-stu-id="b69a2-108">**Dependencies**</span></span>
<span data-ttu-id="b69a2-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-110">必須載入以載入此服務之服務或載入群組之 **BSTR** 名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="b69a2-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="b69a2-111">專案的語法為 "Service："，後面接著服務名稱或 "Group："，後面接著載入組名。</span><span class="sxs-lookup"><span data-stu-id="b69a2-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="b69a2-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-113">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="b69a2-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b69a2-114">**DisplayName**</span></span>
<span data-ttu-id="b69a2-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-116">服務的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a2-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="b69a2-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="b69a2-119">**ErrorControl**</span></span>
<span data-ttu-id="b69a2-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-121">當此服務啟動時，要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="b69a2-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="b69a2-122">以下是這個屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="b69a2-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="b69a2-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ADS \_ 服務 \_ 錯誤 \_ 略過 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-124">啟動程式會記錄錯誤，但會繼續執行啟動操作。</span><span class="sxs-lookup"><span data-stu-id="b69a2-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="b69a2-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>ADS \_ 服務 \_ 錯誤 \_ 一般 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-126">啟動程式會記錄錯誤並顯示訊息方塊，但會繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="b69a2-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="b69a2-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>ADS \_ 服務 \_ 錯誤 \_ 嚴重 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-128">啟動程式會記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a2-128">The startup program logs the error.</span></span> <span data-ttu-id="b69a2-129">如果啟動最後一個已知良好的設定，則會繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="b69a2-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="b69a2-130">否則，系統會重新開機，並使用最後一個已知的正確設定。</span><span class="sxs-lookup"><span data-stu-id="b69a2-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="b69a2-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>ADS \_ 服務 \_ 錯誤 \_ 嚴重 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-132">啟動程式會盡可能記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="b69a2-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="b69a2-133">如果正在啟動最後一個已知良好的設定，則啟動作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="b69a2-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="b69a2-134">否則，系統會重新開機，並使用最後一個已知的正確設定。</span><span class="sxs-lookup"><span data-stu-id="b69a2-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="b69a2-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-136">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b69a2-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-137">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="b69a2-137">**HostComputer**</span></span>
<span data-ttu-id="b69a2-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-139">這項服務的主機 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="b69a2-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="b69a2-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-141">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="b69a2-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="b69a2-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-144">此服務所屬的載入順序群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a2-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="b69a2-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-146">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-147">**路徑**</span><span class="sxs-lookup"><span data-stu-id="b69a2-147">**Path**</span></span>
<span data-ttu-id="b69a2-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-149">此服務之可執行檔的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="b69a2-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="b69a2-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-151">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="b69a2-152">**ServiceAccountName**</span></span>
<span data-ttu-id="b69a2-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-154">這項服務在啟動時用來自行驗證的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b69a2-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="b69a2-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-156">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-157">**ServiceAccountPath**</span><span class="sxs-lookup"><span data-stu-id="b69a2-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="b69a2-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-159">**ServiceAccountPath** 屬性所指定的帳號路徑。</span><span class="sxs-lookup"><span data-stu-id="b69a2-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="b69a2-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-161">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="b69a2-162">**ServiceType**</span></span>
<span data-ttu-id="b69a2-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-164">說明服務如何在主機電腦上呈現本身。</span><span class="sxs-lookup"><span data-stu-id="b69a2-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="b69a2-165">這個屬性可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="b69a2-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="b69a2-166">ADS \_ 服務 \_ 核心 \_ 驅動程式 \* \* \* (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="b69a2-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="b69a2-167">ADS \_ 服務 \_ 檔 \_ 系統 \_ 驅動程式 \* \* \* (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="b69a2-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="b69a2-168">ADS \_ 服務 \_ 自己的 \_ 進程 \* \* \* \* (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="b69a2-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="b69a2-169">ADS \_ 服務 \_ 共用 \_ 進程 \* \* \* (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="b69a2-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="b69a2-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-171">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b69a2-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-172">**StartType**</span><span class="sxs-lookup"><span data-stu-id="b69a2-172">**StartType**</span></span>
<span data-ttu-id="b69a2-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-174">決定如何啟動服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-174">Determines how to start the service.</span></span> <span data-ttu-id="b69a2-175">以下是這個屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="b69a2-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="b69a2-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>ADS \_ 服務 \_ 開機 \_ 啟動 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-177">此服務是由系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b69a2-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="b69a2-178">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="b69a2-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>ADS \_ 服務 \_ 系統 \_ 啟動 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-180">此服務是 **IoInitSystem** 函式所啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b69a2-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="b69a2-181">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="b69a2-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>ADS \_ 服務 \_ 自動 \_ 啟動 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-183">服務控制管理員會在系統啟動期間自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="b69a2-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>ADS \_ 服務 \_ 需求 \_ 開始 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-185">當進程呼叫 [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) 函式時，服務控制管理員會啟動服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="b69a2-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>ADS \_ 服務 \_ 已停用 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b69a2-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b69a2-187">無法啟動服務。</span><span class="sxs-lookup"><span data-stu-id="b69a2-187">The service cannot be started.</span></span> <span data-ttu-id="b69a2-188">嘗試啟動服務會導致錯誤碼 **錯誤 \_ 服務 \_ 停用**。</span><span class="sxs-lookup"><span data-stu-id="b69a2-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="b69a2-189">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-190">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b69a2-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="b69a2-191">**StartupParameters**</span></span>
<span data-ttu-id="b69a2-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-193">啟動時傳遞至服務的參數。</span><span class="sxs-lookup"><span data-stu-id="b69a2-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="b69a2-194">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-195">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b69a2-196">**版本**</span><span class="sxs-lookup"><span data-stu-id="b69a2-196">**Version**</span></span>
<span data-ttu-id="b69a2-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b69a2-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="b69a2-198">服務的版本。</span><span class="sxs-lookup"><span data-stu-id="b69a2-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="b69a2-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b69a2-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b69a2-200">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b69a2-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="b69a2-201">範例</span><span class="sxs-lookup"><span data-stu-id="b69a2-201">Examples</span></span>

<span data-ttu-id="b69a2-202">下列程式碼範例示範如何列出主機電腦上執行的所有可用系統服務 "myMachine"，以及用來尋找服務可執行檔的位置。</span><span class="sxs-lookup"><span data-stu-id="b69a2-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b69a2-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="b69a2-203">Requirements</span></span>



| <span data-ttu-id="b69a2-204">需求</span><span class="sxs-lookup"><span data-stu-id="b69a2-204">Requirement</span></span> | <span data-ttu-id="b69a2-205">值</span><span class="sxs-lookup"><span data-stu-id="b69a2-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b69a2-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b69a2-206">Minimum supported client</span></span><br/> | <span data-ttu-id="b69a2-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b69a2-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b69a2-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b69a2-208">Minimum supported server</span></span><br/> | <span data-ttu-id="b69a2-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b69a2-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b69a2-210">標頭</span><span class="sxs-lookup"><span data-stu-id="b69a2-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="b69a2-211"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="b69a2-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b69a2-212">DLL</span><span class="sxs-lookup"><span data-stu-id="b69a2-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b69a2-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b69a2-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b69a2-214">IID</span><span class="sxs-lookup"><span data-stu-id="b69a2-214">IID</span></span><br/>                      | <span data-ttu-id="b69a2-215">IID \_ IADsService 定義為68AF66E0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="b69a2-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b69a2-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b69a2-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69a2-217">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="b69a2-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="b69a2-218">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="b69a2-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

