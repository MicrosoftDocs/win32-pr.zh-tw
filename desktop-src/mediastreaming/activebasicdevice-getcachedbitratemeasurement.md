---
title: 'ActiveBasicDevice GetCachedBitrateMeasurement 方法 (PlayToDevice .h) '
description: 取得快取的位元速率。
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- GetCachedBitrateMeasurement 方法媒體串流 API
- GetCachedBitrateMeasurement 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetCachedBitrateMeasurement 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509191"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="34b9b-106">ActiveBasicDevice：： GetCachedBitrateMeasurement 方法</span><span class="sxs-lookup"><span data-stu-id="34b9b-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="34b9b-107">取得快取的位元速率。</span><span class="sxs-lookup"><span data-stu-id="34b9b-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="34b9b-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="34b9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="34b9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b9b-110">*physicalNetworkInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34b9b-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34b9b-111">指定實體網路介面。</span><span class="sxs-lookup"><span data-stu-id="34b9b-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="34b9b-112">*位元速率* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="34b9b-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="34b9b-113">接收位元速率值。</span><span class="sxs-lookup"><span data-stu-id="34b9b-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34b9b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="34b9b-114">Return value</span></span>

<span data-ttu-id="34b9b-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="34b9b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34b9b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="34b9b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b9b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="34b9b-117">Requirements</span></span>



| <span data-ttu-id="34b9b-118">需求</span><span class="sxs-lookup"><span data-stu-id="34b9b-118">Requirement</span></span> | <span data-ttu-id="34b9b-119">值</span><span class="sxs-lookup"><span data-stu-id="34b9b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b9b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34b9b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34b9b-121">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34b9b-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="34b9b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34b9b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34b9b-123">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34b9b-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34b9b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="34b9b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34b9b-125"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="34b9b-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="34b9b-126">Idl</span><span class="sxs-lookup"><span data-stu-id="34b9b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34b9b-127"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="34b9b-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="34b9b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="34b9b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34b9b-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34b9b-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b9b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34b9b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="34b9b-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34b9b-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

