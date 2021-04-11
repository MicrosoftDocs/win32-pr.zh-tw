---
description: 刪除指定的掃描設定檔。
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'IScanProfileMgr：:D eleteProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944318"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="e9db5-103">IScanProfileMgr：:D eleteProfile 方法</span><span class="sxs-lookup"><span data-stu-id="e9db5-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="e9db5-104">刪除指定的掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="e9db5-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9db5-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9db5-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="e9db5-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9db5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9db5-107">*pScanProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9db5-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9db5-108">類型： \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="e9db5-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="e9db5-109">設定檔的指標。</span><span class="sxs-lookup"><span data-stu-id="e9db5-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9db5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9db5-110">Return value</span></span>

<span data-ttu-id="e9db5-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e9db5-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e9db5-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e9db5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9db5-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9db5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9db5-114">備註</span><span class="sxs-lookup"><span data-stu-id="e9db5-114">Remarks</span></span>

<span data-ttu-id="e9db5-115">**IScanProfileMgr：:D eleteprofile** 會從磁片刪除設定檔，並在記憶體中終結設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="e9db5-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="e9db5-116">當有一個以上的 [**IScanProfileMgr**](-wia-iscanprofilemgr.md)物件可能同時建立或刪除設定檔時，請使用 [**IScanProfileMgr：： Refresh**](-wia-iscanprofilemgr-refresh.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e9db5-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9db5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9db5-117">Requirements</span></span>



| <span data-ttu-id="e9db5-118">需求</span><span class="sxs-lookup"><span data-stu-id="e9db5-118">Requirement</span></span> | <span data-ttu-id="e9db5-119">值</span><span class="sxs-lookup"><span data-stu-id="e9db5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9db5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9db5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9db5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9db5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e9db5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9db5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9db5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9db5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9db5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e9db5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9db5-125"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9db5-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="e9db5-126">Idl</span><span class="sxs-lookup"><span data-stu-id="e9db5-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9db5-127"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9db5-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9db5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9db5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9db5-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="e9db5-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="e9db5-130">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="e9db5-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




