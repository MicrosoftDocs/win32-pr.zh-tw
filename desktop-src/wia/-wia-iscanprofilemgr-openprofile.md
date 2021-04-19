---
description: 開啟已儲存至磁片的掃描設定檔做為 XML 檔案。
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'IScanProfileMgr：： OpenProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980865"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="153a0-103">IScanProfileMgr：： OpenProfile 方法</span><span class="sxs-lookup"><span data-stu-id="153a0-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="153a0-104">開啟已儲存至磁片的掃描設定檔做為 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="153a0-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="153a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="153a0-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="153a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="153a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153a0-107">*guid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="153a0-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153a0-108">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="153a0-108">Type: **GUID**</span></span>

<span data-ttu-id="153a0-109">設定檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="153a0-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="153a0-110">*ppScanProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="153a0-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153a0-111">類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="153a0-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="153a0-112">設定檔指標的位址。</span><span class="sxs-lookup"><span data-stu-id="153a0-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="153a0-113">Return value</span></span>

<span data-ttu-id="153a0-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="153a0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="153a0-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="153a0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="153a0-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="153a0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="153a0-117">備註</span><span class="sxs-lookup"><span data-stu-id="153a0-117">Remarks</span></span>

<span data-ttu-id="153a0-118">如果使用 [**Save**](-wia-iscanprofile-save.md) 方法儲存掃描設定檔，它會儲存為 XML 檔案，位於% USERPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ Document Center \\ UserScanProfiles。</span><span class="sxs-lookup"><span data-stu-id="153a0-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="153a0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="153a0-119">Requirements</span></span>



| <span data-ttu-id="153a0-120">需求</span><span class="sxs-lookup"><span data-stu-id="153a0-120">Requirement</span></span> | <span data-ttu-id="153a0-121">值</span><span class="sxs-lookup"><span data-stu-id="153a0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="153a0-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="153a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="153a0-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="153a0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="153a0-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="153a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="153a0-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="153a0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="153a0-126">標頭</span><span class="sxs-lookup"><span data-stu-id="153a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="153a0-127"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="153a0-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="153a0-128">Idl</span><span class="sxs-lookup"><span data-stu-id="153a0-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="153a0-129"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="153a0-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153a0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="153a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153a0-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="153a0-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="153a0-132">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="153a0-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




