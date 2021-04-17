---
description: 傳回設定檔的 GUID。
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'IScanProfile：： GetGUID 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318580"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="2bc44-103">IScanProfile：： GetGUID 方法</span><span class="sxs-lookup"><span data-stu-id="2bc44-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="2bc44-104">傳回設定檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2bc44-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc44-105">語法</span><span class="sxs-lookup"><span data-stu-id="2bc44-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="2bc44-106">參數</span><span class="sxs-lookup"><span data-stu-id="2bc44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc44-107">*retVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2bc44-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc44-108">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="2bc44-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="2bc44-109">設定檔 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="2bc44-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc44-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bc44-110">Return value</span></span>

<span data-ttu-id="2bc44-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2bc44-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2bc44-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2bc44-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2bc44-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2bc44-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc44-114">備註</span><span class="sxs-lookup"><span data-stu-id="2bc44-114">Remarks</span></span>

<span data-ttu-id="2bc44-115">使用 [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)建立設定檔時，會自動產生設定檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2bc44-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc44-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bc44-116">Requirements</span></span>



| <span data-ttu-id="2bc44-117">需求</span><span class="sxs-lookup"><span data-stu-id="2bc44-117">Requirement</span></span> | <span data-ttu-id="2bc44-118">值</span><span class="sxs-lookup"><span data-stu-id="2bc44-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc44-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bc44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc44-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc44-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2bc44-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bc44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc44-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc44-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bc44-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2bc44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc44-124"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc44-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="2bc44-125">Idl</span><span class="sxs-lookup"><span data-stu-id="2bc44-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bc44-126"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bc44-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc44-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bc44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc44-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="2bc44-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="2bc44-129">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="2bc44-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




