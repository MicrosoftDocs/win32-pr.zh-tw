---
description: 取得預設掃描設定檔。
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'IScanProfileMgr：： GetDefaultProfile 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983336"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a><span data-ttu-id="a4b61-103">IScanProfileMgr：： GetDefaultProfile 方法</span><span class="sxs-lookup"><span data-stu-id="a4b61-103">IScanProfileMgr::GetDefaultProfile method</span></span>

<span data-ttu-id="a4b61-104">取得預設掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="a4b61-104">Gets the default scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b61-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4b61-105">Syntax</span></span>


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="a4b61-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b61-107">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4b61-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b61-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a4b61-108">Type: **BSTR**</span></span>

<span data-ttu-id="a4b61-109">裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4b61-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="a4b61-110">*ppScanProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4b61-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b61-111">類型： **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a4b61-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="a4b61-112">裝置預設設定檔指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a4b61-112">The address of a pointer to the device's default profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b61-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4b61-113">Return value</span></span>

<span data-ttu-id="a4b61-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a4b61-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a4b61-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a4b61-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4b61-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a4b61-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b61-117">備註</span><span class="sxs-lookup"><span data-stu-id="a4b61-117">Remarks</span></span>

<span data-ttu-id="a4b61-118">預設設定檔有一個 `<Default>` 元素。</span><span class="sxs-lookup"><span data-stu-id="a4b61-118">The default profile has a `<Default>` element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b61-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4b61-119">Requirements</span></span>



| <span data-ttu-id="a4b61-120">需求</span><span class="sxs-lookup"><span data-stu-id="a4b61-120">Requirement</span></span> | <span data-ttu-id="a4b61-121">值</span><span class="sxs-lookup"><span data-stu-id="a4b61-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b61-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4b61-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b61-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b61-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a4b61-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4b61-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b61-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b61-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4b61-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a4b61-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b61-127"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b61-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="a4b61-128">Idl</span><span class="sxs-lookup"><span data-stu-id="a4b61-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4b61-129"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4b61-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b61-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b61-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b61-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="a4b61-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="a4b61-132">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="a4b61-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




