---
description: SetQOSApplicationID 方法會設定應用程式的 QOS 識別碼。
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID：： SetQOSApplicationID 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979477"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="fc848-103">ITQOSApplicationID：： SetQOSApplicationID 方法</span><span class="sxs-lookup"><span data-stu-id="fc848-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="fc848-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fc848-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc848-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fc848-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fc848-106">**SetQOSApplicationID** 方法會設定應用程式的 QOS 識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc848-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc848-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc848-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="fc848-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc848-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc848-109">*pApplicationID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc848-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc848-110">應用程式進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc848-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="fc848-111">*pApplicationGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc848-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc848-112">應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="fc848-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="fc848-113">*pSubIDs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc848-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc848-114">與目前呼叫相關聯的 Sub-IDs。</span><span class="sxs-lookup"><span data-stu-id="fc848-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc848-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc848-115">Return value</span></span>

<span data-ttu-id="fc848-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fc848-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fc848-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fc848-117">Return code</span></span>                                                                                   | <span data-ttu-id="fc848-118">Description</span><span class="sxs-lookup"><span data-stu-id="fc848-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fc848-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fc848-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fc848-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="fc848-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fc848-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fc848-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fc848-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="fc848-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc848-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc848-123">Requirements</span></span>



| <span data-ttu-id="fc848-124">需求</span><span class="sxs-lookup"><span data-stu-id="fc848-124">Requirement</span></span> | <span data-ttu-id="fc848-125">值</span><span class="sxs-lookup"><span data-stu-id="fc848-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc848-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fc848-126">TAPI version</span></span><br/> | <span data-ttu-id="fc848-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="fc848-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="fc848-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fc848-128">Header</span></span><br/>       | <dl> <span data-ttu-id="fc848-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc848-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc848-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc848-130">Library</span></span><br/>      | <dl> <span data-ttu-id="fc848-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="fc848-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="fc848-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fc848-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="fc848-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc848-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc848-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc848-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc848-135">**ITQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="fc848-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




