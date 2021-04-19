---
description: 安裝例外狀況套件。
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990712"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="1e6c4-103">InstallComponentW 函式</span><span class="sxs-lookup"><span data-stu-id="1e6c4-103">InstallComponentW function</span></span>

<span data-ttu-id="1e6c4-104">安裝例外狀況套件。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="1e6c4-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="1e6c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="1e6c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e6c4-107">*InfPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-108">要處理之例外狀況 INF 的路徑。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-109">*CompGuid* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-110">要安裝之例外狀況元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-112">用來控制安裝行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="1e6c4-113">這個參數可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="1e6c4-114">值</span><span class="sxs-lookup"><span data-stu-id="1e6c4-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="1e6c4-115">意義</span><span class="sxs-lookup"><span data-stu-id="1e6c4-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="1e6c4-116"><dt>**COMP \_旗標 \_ 強制**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="1e6c4-117">略過檔案取代的版本檢查。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="1e6c4-118"><dt>**COMP \_旗標 \_ 需要 \_ 卸載**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="1e6c4-119">備份檔案，以供卸載元件時使用。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="1e6c4-120"><dt>**COMP \_旗標 \_ 無 \_ 覆寫**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="1e6c4-121">如果例外狀況元件版本與已安裝的元件相同，則略過備份檔案。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="1e6c4-122">此旗標用於重新安裝案例中。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="1e6c4-123"><dt>**COMP \_旗標 \_ NOUI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="1e6c4-124">隱藏所有 UI。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="1e6c4-125"><dt>**COMP \_旗標 \_ 更新 \_ DLLCACHE**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="1e6c4-126">當更新系統檔案時，強制更新 DLLCACHE 目錄。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="1e6c4-127"><dt>**COMP \_旗 \_ 標 \_ 使用 \_ SVCPACK**</dt>快取 <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="1e6c4-128">使用 Windows service pack 安裝所快取的檔案來取代備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="1e6c4-129">*>vermajor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-130">例外狀況元件的主要版本。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-131">*>verminor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-132">例外狀況元件的次要版本。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-133">*VerBuild* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-134">例外狀況元件的組建版本。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-135">*VerQFE* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-136">例外狀況元件的修正程式修訂。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1e6c4-137">*名稱* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1e6c4-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6c4-138">如果作業系統偵測到 Windows 檔案保護保護檔案已損毀、遭篡改或損毀，Windows 檔案保護對話方塊所顯示之元件的描述性字串。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e6c4-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e6c4-139">Return value</span></span>

<span data-ttu-id="1e6c4-140">此函式會傳回 **HRESULT** 值， (S \_ OK 或失敗碼) 。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="1e6c4-141">您可以針對0x20000100 值檢查失敗碼，以判斷失敗是否因為需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6c4-142">備註</span><span class="sxs-lookup"><span data-stu-id="1e6c4-142">Remarks</span></span>

<span data-ttu-id="1e6c4-143">例外狀況套件是 Windows 系統檔案，這些檔案是在完整套件 Windows 版本之外發行，而且會更新作業系統檔案。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="1e6c4-144">例外狀況套件只是由已獲得授權更新 Windows 系統檔案的作業系統小組所撰寫。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="1e6c4-145">若要安裝和卸載未受 Windows 檔案保護保護的檔案，請使用 [一般安裝](https://msdn.microsoft.com/library/ms794585.aspx)函式中記載的功能。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="1e6c4-146">若要安裝設備磁碟機，venders 應該使用 [裝置安裝功能](https://msdn.microsoft.com/library/ms792954.aspx) 和 [PnP 設定管理員](https://msdn.microsoft.com/library/ms790838.aspx)函式中記載的功能。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="1e6c4-147">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="1e6c4-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6c4-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e6c4-148">Requirements</span></span>



| <span data-ttu-id="1e6c4-149">需求</span><span class="sxs-lookup"><span data-stu-id="1e6c4-149">Requirement</span></span> | <span data-ttu-id="1e6c4-150">值</span><span class="sxs-lookup"><span data-stu-id="1e6c4-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6c4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1e6c4-151">DLL</span></span><br/> | <dl> <span data-ttu-id="1e6c4-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e6c4-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
