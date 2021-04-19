---
description: 移除例外狀況套件。
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974930"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="ffad8-103">UninstallComponent 函式</span><span class="sxs-lookup"><span data-stu-id="ffad8-103">UninstallComponent function</span></span>

<span data-ttu-id="ffad8-104">移除例外狀況套件。</span><span class="sxs-lookup"><span data-stu-id="ffad8-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffad8-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffad8-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="ffad8-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffad8-107">*CompGuid* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-108">要卸載之例外狀況元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ffad8-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="ffad8-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-110">用來控制安裝行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="ffad8-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="ffad8-111">這個參數可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="ffad8-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="ffad8-112">值</span><span class="sxs-lookup"><span data-stu-id="ffad8-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="ffad8-113">意義</span><span class="sxs-lookup"><span data-stu-id="ffad8-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="ffad8-114"><dt>**COMP \_ 旗標 \_ NOUI**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="ffad8-115">隱藏所有 UI。</span><span class="sxs-lookup"><span data-stu-id="ffad8-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="ffad8-116"><dt>**COMP \_ 旗標 \_ 更新 \_ DLLCACHE**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="ffad8-117">當更新系統檔案時，強制更新 DLLCACHE 目錄。</span><span class="sxs-lookup"><span data-stu-id="ffad8-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="ffad8-118"><dt>**使用 SVCPACK 快取的複合 \_ 旗標 \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="ffad8-119">使用 Windows service pack 安裝所快取的檔案來取代備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="ffad8-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ffad8-120">*>vermajor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-121">要卸載之例外狀況元件的主要版本。</span><span class="sxs-lookup"><span data-stu-id="ffad8-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="ffad8-122">*>verminor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-123">要卸載之例外狀況元件的次要版本。</span><span class="sxs-lookup"><span data-stu-id="ffad8-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="ffad8-124">*VerBuild* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-125">要卸載之例外狀況元件的組建版本。</span><span class="sxs-lookup"><span data-stu-id="ffad8-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="ffad8-126">*VerQFE* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad8-127">要卸載之例外狀況元件的修正程式修訂。</span><span class="sxs-lookup"><span data-stu-id="ffad8-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffad8-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffad8-128">Return value</span></span>

<span data-ttu-id="ffad8-129">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ffad8-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffad8-130">備註</span><span class="sxs-lookup"><span data-stu-id="ffad8-130">Remarks</span></span>

<span data-ttu-id="ffad8-131">例外狀況套件是 Windows 系統檔案，這些檔案是在完整套件 Windows 版本之外發行，而且會更新作業系統檔案。</span><span class="sxs-lookup"><span data-stu-id="ffad8-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="ffad8-132">例外狀況套件只是由已獲得授權更新 Windows 系統檔案的作業系統小組所撰寫。</span><span class="sxs-lookup"><span data-stu-id="ffad8-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="ffad8-133">若要安裝和卸載未受 Windows 檔案保護保護的檔案，請使用 [一般安裝](https://msdn.microsoft.com/library/ms794585.aspx)函式中記載的功能。</span><span class="sxs-lookup"><span data-stu-id="ffad8-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="ffad8-134">若要安裝設備磁碟機，venders 應該使用 [裝置安裝功能](https://msdn.microsoft.com/library/ms792954.aspx) 和 [PnP 設定管理員](https://msdn.microsoft.com/library/ms790838.aspx)函式中記載的功能。</span><span class="sxs-lookup"><span data-stu-id="ffad8-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="ffad8-135">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ffad8-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffad8-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffad8-136">Requirements</span></span>



| <span data-ttu-id="ffad8-137">需求</span><span class="sxs-lookup"><span data-stu-id="ffad8-137">Requirement</span></span> | <span data-ttu-id="ffad8-138">值</span><span class="sxs-lookup"><span data-stu-id="ffad8-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffad8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ffad8-139">DLL</span></span><br/> | <dl> <span data-ttu-id="ffad8-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffad8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffad8-141">See also</span></span>

<dl> <span data-ttu-id="ffad8-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ffad8-143">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="ffad8-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
