---
description: 建立空的掃描設定檔，並將它與掃描器或其他 Windows 映像取得 (WIA) 2.0 專案產生關聯。
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr：： CreateProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469233"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="c7ebf-103">IScanProfileMgr：： CreateProfile 方法</span><span class="sxs-lookup"><span data-stu-id="c7ebf-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="c7ebf-104">建立空的掃描設定檔，並將它與掃描器或其他 Windows 映像取得 (WIA) 2.0 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ebf-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7ebf-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="c7ebf-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7ebf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7ebf-107">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ebf-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c7ebf-108">Type: **BSTR**</span></span>

<span data-ttu-id="c7ebf-109">裝置或 WIA 2.0 專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="c7ebf-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ebf-111">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c7ebf-111">Type: **BSTR**</span></span>

<span data-ttu-id="c7ebf-112">新設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="c7ebf-113">*guidCategory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ebf-114">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="c7ebf-114">Type: **GUID**</span></span>

<span data-ttu-id="c7ebf-115">裝置或 WIA 2.0 專案類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="c7ebf-116">這必須是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="c7ebf-117">*ppScanProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ebf-118">類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c7ebf-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="c7ebf-119">新設定檔指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7ebf-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7ebf-120">Return value</span></span>

<span data-ttu-id="c7ebf-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c7ebf-121">Type: **HRESULT**</span></span>

<span data-ttu-id="c7ebf-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7ebf-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7ebf-124">備註</span><span class="sxs-lookup"><span data-stu-id="c7ebf-124">Remarks</span></span>

<span data-ttu-id="c7ebf-125">**IScanProfileMgr：： CreateProfile** 會將指定的裝置與新的掃描設定檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="c7ebf-126">**IScanProfileMgr：： CreateProfile** 會自動產生新設定檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="c7ebf-127">使用 [**GetGUID**](-wia-iscanprofile-getguid.md)取得 GUID。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="c7ebf-128">當有一個以上的 [**IScanProfileMgr**](-wia-iscanprofilemgr.md)物件可能同時建立或刪除設定檔時，請使用 [**IScanProfileMgr：： Refresh**](-wia-iscanprofilemgr-refresh.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c7ebf-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ebf-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7ebf-129">Requirements</span></span>



| <span data-ttu-id="c7ebf-130">需求</span><span class="sxs-lookup"><span data-stu-id="c7ebf-130">Requirement</span></span> | <span data-ttu-id="c7ebf-131">值</span><span class="sxs-lookup"><span data-stu-id="c7ebf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ebf-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7ebf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ebf-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c7ebf-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7ebf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ebf-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7ebf-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7ebf-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c7ebf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ebf-137"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ebf-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="c7ebf-138">Idl</span><span class="sxs-lookup"><span data-stu-id="c7ebf-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7ebf-139"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7ebf-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ebf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7ebf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ebf-141">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="c7ebf-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="c7ebf-142">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="c7ebf-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




