---
description: 取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr：： >ipartner.getprofiles 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693071"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="f4d76-103">IScanProfileMgr：： >ipartner.getprofiles 方法</span><span class="sxs-lookup"><span data-stu-id="f4d76-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="f4d76-104">取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="f4d76-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4d76-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4d76-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="f4d76-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4d76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4d76-107">*pulNumProfiles* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f4d76-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4d76-108">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="f4d76-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f4d76-109">傳遞時，為要傳回的最大設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="f4d76-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="f4d76-110">傳回時，為所傳回設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="f4d76-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="f4d76-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f4d76-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4d76-112">類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f4d76-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="f4d76-113">設定檔指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="f4d76-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4d76-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4d76-114">Return value</span></span>

<span data-ttu-id="f4d76-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f4d76-115">Type: **HRESULT**</span></span>

<span data-ttu-id="f4d76-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f4d76-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4d76-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f4d76-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d76-118">備註</span><span class="sxs-lookup"><span data-stu-id="f4d76-118">Remarks</span></span>

<span data-ttu-id="f4d76-119">如果使用者可用的設定檔總數小於傳遞給 *pulNumProfiles* 的值，則 *pulNumProfiles* 會傳回該總計。</span><span class="sxs-lookup"><span data-stu-id="f4d76-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="f4d76-120">否則，它會傳回與傳遞給它相同的值。</span><span class="sxs-lookup"><span data-stu-id="f4d76-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d76-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4d76-121">Requirements</span></span>



| <span data-ttu-id="f4d76-122">需求</span><span class="sxs-lookup"><span data-stu-id="f4d76-122">Requirement</span></span> | <span data-ttu-id="f4d76-123">值</span><span class="sxs-lookup"><span data-stu-id="f4d76-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d76-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4d76-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f4d76-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4d76-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f4d76-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4d76-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f4d76-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4d76-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4d76-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f4d76-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4d76-129"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4d76-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f4d76-130">Idl</span><span class="sxs-lookup"><span data-stu-id="f4d76-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4d76-131"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4d76-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4d76-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4d76-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4d76-133">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="f4d76-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f4d76-134">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="f4d76-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




