---
description: 取得與裝置相關聯的所有掃描設定檔。
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'IScanProfileMgr：： GetProfilesforDeviceID 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966755"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="4bde8-103">IScanProfileMgr：： GetProfilesforDeviceID 方法</span><span class="sxs-lookup"><span data-stu-id="4bde8-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="4bde8-104">取得與裝置相關聯的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="4bde8-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bde8-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bde8-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="4bde8-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bde8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bde8-107">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bde8-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bde8-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4bde8-108">Type: **BSTR**</span></span>

<span data-ttu-id="4bde8-109">裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bde8-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="4bde8-110">*pulNumProfiles* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4bde8-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bde8-111">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="4bde8-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="4bde8-112">傳遞時，為要傳回的最大設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="4bde8-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="4bde8-113">傳回時，為所傳回設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="4bde8-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="4bde8-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4bde8-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bde8-115">類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4bde8-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="4bde8-116">設定檔陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="4bde8-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bde8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bde8-117">Return value</span></span>

<span data-ttu-id="4bde8-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4bde8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4bde8-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4bde8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bde8-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4bde8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bde8-121">備註</span><span class="sxs-lookup"><span data-stu-id="4bde8-121">Remarks</span></span>

<span data-ttu-id="4bde8-122">如果與裝置相關聯的設定檔總數小於傳遞給 *pulNumProfiles* 的值，則 *pulNumProfiles* 會傳回該總計。</span><span class="sxs-lookup"><span data-stu-id="4bde8-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="4bde8-123">否則，它會傳回與傳遞給它相同的值。</span><span class="sxs-lookup"><span data-stu-id="4bde8-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bde8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bde8-124">Requirements</span></span>



| <span data-ttu-id="4bde8-125">需求</span><span class="sxs-lookup"><span data-stu-id="4bde8-125">Requirement</span></span> | <span data-ttu-id="4bde8-126">值</span><span class="sxs-lookup"><span data-stu-id="4bde8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bde8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bde8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4bde8-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bde8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4bde8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bde8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4bde8-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bde8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bde8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="4bde8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bde8-132"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bde8-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="4bde8-133">Idl</span><span class="sxs-lookup"><span data-stu-id="4bde8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4bde8-134"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4bde8-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bde8-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bde8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bde8-136">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="4bde8-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="4bde8-137">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="4bde8-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




