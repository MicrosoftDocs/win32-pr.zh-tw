---
description: 傳回裝置的識別碼。
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'IScanProfile：： GetDeviceID 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318583"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="0a746-103">IScanProfile：： GetDeviceID 方法</span><span class="sxs-lookup"><span data-stu-id="0a746-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="0a746-104">傳回裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a746-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a746-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a746-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="0a746-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a746-107">*pbstrDeviceID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a746-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a746-108">類型： \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="0a746-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="0a746-109">裝置識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="0a746-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a746-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a746-110">Return value</span></span>

<span data-ttu-id="0a746-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0a746-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0a746-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0a746-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a746-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a746-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a746-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a746-114">Requirements</span></span>



| <span data-ttu-id="0a746-115">需求</span><span class="sxs-lookup"><span data-stu-id="0a746-115">Requirement</span></span> | <span data-ttu-id="0a746-116">值</span><span class="sxs-lookup"><span data-stu-id="0a746-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a746-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a746-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a746-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a746-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0a746-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a746-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a746-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a746-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a746-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0a746-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a746-122"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a746-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="0a746-123">Idl</span><span class="sxs-lookup"><span data-stu-id="0a746-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a746-124"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a746-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a746-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a746-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a746-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="0a746-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="0a746-127">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="0a746-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




