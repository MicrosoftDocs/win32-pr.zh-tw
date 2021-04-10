---
title: 'ActiveBasicDevice GetEffectiveBandwidth 方法 (PlayToDevice .h) '
description: 取得裝置目前有效的頻寬。
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- GetEffectiveBandwidth 方法媒體串流 API
- GetEffectiveBandwidth 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetEffectiveBandwidth 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025447"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="12ec8-106">ActiveBasicDevice：： GetEffectiveBandwidth 方法</span><span class="sxs-lookup"><span data-stu-id="12ec8-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="12ec8-107">取得裝置目前有效的頻寬。</span><span class="sxs-lookup"><span data-stu-id="12ec8-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ec8-108">語法</span><span class="sxs-lookup"><span data-stu-id="12ec8-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="12ec8-109">參數</span><span class="sxs-lookup"><span data-stu-id="12ec8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ec8-110">*transmitSpeed* \[在中，retval\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="12ec8-111">指定是否抓取傳送速率或抓取接收速度。</span><span class="sxs-lookup"><span data-stu-id="12ec8-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="12ec8-112">**true** 表示取得傳送速率。</span><span class="sxs-lookup"><span data-stu-id="12ec8-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="12ec8-113">**false** 表示取得接收速度。</span><span class="sxs-lookup"><span data-stu-id="12ec8-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="12ec8-114">*currentSpeed* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12ec8-115">接收目前有效的頻寬。</span><span class="sxs-lookup"><span data-stu-id="12ec8-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ec8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="12ec8-116">Return value</span></span>

<span data-ttu-id="12ec8-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="12ec8-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12ec8-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12ec8-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ec8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="12ec8-119">Requirements</span></span>



| <span data-ttu-id="12ec8-120">需求</span><span class="sxs-lookup"><span data-stu-id="12ec8-120">Requirement</span></span> | <span data-ttu-id="12ec8-121">值</span><span class="sxs-lookup"><span data-stu-id="12ec8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="12ec8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12ec8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12ec8-123">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="12ec8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12ec8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12ec8-125">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12ec8-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="12ec8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="12ec8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ec8-127"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="12ec8-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="12ec8-128">Idl</span><span class="sxs-lookup"><span data-stu-id="12ec8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12ec8-129"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="12ec8-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="12ec8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="12ec8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12ec8-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ec8-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ec8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12ec8-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="12ec8-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12ec8-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

