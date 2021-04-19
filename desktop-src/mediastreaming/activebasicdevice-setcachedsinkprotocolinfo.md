---
title: 'ActiveBasicDevice SetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
description: '取得裝置的快取接收通訊協定資訊。 |ActiveBasicDevice SetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- SetCachedSinkProtocolInfo 方法媒體串流 API
- SetCachedSinkProtocolInfo 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，SetCachedSinkProtocolInfo 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988567"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="4a69a-107">ActiveBasicDevice：： SetCachedSinkProtocolInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4a69a-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="4a69a-108">取得裝置的快取接收通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="4a69a-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a69a-109">語法</span><span class="sxs-lookup"><span data-stu-id="4a69a-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="4a69a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a69a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a69a-111">*physicalNetworkInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a69a-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a69a-112">指定實體網路介面。</span><span class="sxs-lookup"><span data-stu-id="4a69a-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="4a69a-113">*位元速率* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a69a-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a69a-114">位元速率值。</span><span class="sxs-lookup"><span data-stu-id="4a69a-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a69a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a69a-115">Return value</span></span>

<span data-ttu-id="4a69a-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4a69a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a69a-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4a69a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a69a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a69a-118">Requirements</span></span>



| <span data-ttu-id="4a69a-119">需求</span><span class="sxs-lookup"><span data-stu-id="4a69a-119">Requirement</span></span> | <span data-ttu-id="4a69a-120">值</span><span class="sxs-lookup"><span data-stu-id="4a69a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a69a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a69a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4a69a-122">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a69a-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a69a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a69a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4a69a-124">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a69a-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a69a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4a69a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a69a-126"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a69a-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a69a-127">Idl</span><span class="sxs-lookup"><span data-stu-id="4a69a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a69a-128"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a69a-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a69a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4a69a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a69a-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a69a-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a69a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a69a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a69a-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a69a-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

