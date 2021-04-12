---
description: 取得裝置的掃描設定檔數目。
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'IScanProfileMgr：： GetNumProfilesforDeviceID 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191574"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="ddc09-103">IScanProfileMgr：： GetNumProfilesforDeviceID 方法</span><span class="sxs-lookup"><span data-stu-id="ddc09-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="ddc09-104">取得裝置的掃描設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="ddc09-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc09-105">語法</span><span class="sxs-lookup"><span data-stu-id="ddc09-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="ddc09-106">參數</span><span class="sxs-lookup"><span data-stu-id="ddc09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc09-107">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ddc09-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc09-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ddc09-108">Type: **BSTR**</span></span>

<span data-ttu-id="ddc09-109">裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc09-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="ddc09-110">*pulNumProfiles* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ddc09-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc09-111">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="ddc09-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="ddc09-112">裝置可用設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="ddc09-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc09-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ddc09-113">Return value</span></span>

<span data-ttu-id="ddc09-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ddc09-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ddc09-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ddc09-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ddc09-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ddc09-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc09-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddc09-117">Requirements</span></span>



| <span data-ttu-id="ddc09-118">需求</span><span class="sxs-lookup"><span data-stu-id="ddc09-118">Requirement</span></span> | <span data-ttu-id="ddc09-119">值</span><span class="sxs-lookup"><span data-stu-id="ddc09-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc09-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ddc09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc09-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddc09-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ddc09-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ddc09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc09-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddc09-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ddc09-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ddc09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddc09-125"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc09-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="ddc09-126">Idl</span><span class="sxs-lookup"><span data-stu-id="ddc09-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ddc09-127"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ddc09-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc09-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddc09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc09-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="ddc09-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="ddc09-130">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="ddc09-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




