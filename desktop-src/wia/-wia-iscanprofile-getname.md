---
description: 取得設定檔的易記名稱。
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'IScanProfile：： GetName 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191576"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="9e326-103">IScanProfile：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="9e326-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="9e326-104">取得設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9e326-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e326-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e326-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="9e326-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e326-107">*pbstrName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9e326-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e326-108">類型： \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="9e326-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="9e326-109">設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9e326-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e326-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e326-110">Return value</span></span>

<span data-ttu-id="9e326-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9e326-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9e326-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9e326-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e326-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e326-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e326-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e326-114">Remarks</span></span>

<span data-ttu-id="9e326-115">這個方法是必要的，因為設定檔的 GUID 不能用來向使用者顯示掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="9e326-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e326-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e326-116">Requirements</span></span>



| <span data-ttu-id="9e326-117">需求</span><span class="sxs-lookup"><span data-stu-id="9e326-117">Requirement</span></span> | <span data-ttu-id="9e326-118">值</span><span class="sxs-lookup"><span data-stu-id="9e326-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e326-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e326-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e326-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e326-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9e326-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e326-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e326-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e326-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e326-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9e326-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e326-124"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e326-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="9e326-125">Idl</span><span class="sxs-lookup"><span data-stu-id="9e326-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e326-126"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e326-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e326-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e326-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e326-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="9e326-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="9e326-129">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="9e326-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




