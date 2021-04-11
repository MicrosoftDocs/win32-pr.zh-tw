---
description: 刪除與指定裝置相關聯的所有掃描設定檔。
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: 'IScanProfileMgr：:D eleteAllProfiles 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026769"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="fb36d-103">IScanProfileMgr：:D eleteAllProfiles 方法</span><span class="sxs-lookup"><span data-stu-id="fb36d-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="fb36d-104">刪除與指定裝置相關聯的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb36d-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb36d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb36d-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="fb36d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb36d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb36d-107">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb36d-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb36d-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fb36d-108">Type: **BSTR**</span></span>

<span data-ttu-id="fb36d-109">裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb36d-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb36d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb36d-110">Return value</span></span>

<span data-ttu-id="fb36d-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fb36d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fb36d-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fb36d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb36d-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fb36d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb36d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb36d-114">Requirements</span></span>



| <span data-ttu-id="fb36d-115">需求</span><span class="sxs-lookup"><span data-stu-id="fb36d-115">Requirement</span></span> | <span data-ttu-id="fb36d-116">值</span><span class="sxs-lookup"><span data-stu-id="fb36d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb36d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb36d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb36d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb36d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fb36d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb36d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb36d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb36d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb36d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fb36d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb36d-122"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb36d-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="fb36d-123">Idl</span><span class="sxs-lookup"><span data-stu-id="fb36d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb36d-124"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb36d-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb36d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb36d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb36d-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="fb36d-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="fb36d-127">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="fb36d-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




