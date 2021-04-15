---
title: 'ActiveBasicDevice SetCachedBitrateMeasurement 方法 (PlayToDevice .h) '
description: 設定快取的位元速率。
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- SetCachedBitrateMeasurement 方法媒體串流 API
- SetCachedBitrateMeasurement 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，SetCachedBitrateMeasurement 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466813"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="59eb9-106">ActiveBasicDevice：： SetCachedBitrateMeasurement 方法</span><span class="sxs-lookup"><span data-stu-id="59eb9-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="59eb9-107">設定快取的位元速率。</span><span class="sxs-lookup"><span data-stu-id="59eb9-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eb9-108">語法</span><span class="sxs-lookup"><span data-stu-id="59eb9-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="59eb9-109">參數</span><span class="sxs-lookup"><span data-stu-id="59eb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59eb9-110">*physicalNetworkInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="59eb9-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb9-111">指定實體網路介面。</span><span class="sxs-lookup"><span data-stu-id="59eb9-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="59eb9-112">*位元速率* \[在\]</span><span class="sxs-lookup"><span data-stu-id="59eb9-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb9-113">要設定位元速率的值。</span><span class="sxs-lookup"><span data-stu-id="59eb9-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59eb9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="59eb9-114">Return value</span></span>

<span data-ttu-id="59eb9-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="59eb9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59eb9-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59eb9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eb9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="59eb9-117">Requirements</span></span>



| <span data-ttu-id="59eb9-118">需求</span><span class="sxs-lookup"><span data-stu-id="59eb9-118">Requirement</span></span> | <span data-ttu-id="59eb9-119">值</span><span class="sxs-lookup"><span data-stu-id="59eb9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="59eb9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59eb9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59eb9-121">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59eb9-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59eb9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59eb9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59eb9-123">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59eb9-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59eb9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="59eb9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59eb9-125"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="59eb9-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="59eb9-126">Idl</span><span class="sxs-lookup"><span data-stu-id="59eb9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59eb9-127"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="59eb9-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="59eb9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="59eb9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59eb9-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59eb9-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eb9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59eb9-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="59eb9-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59eb9-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

