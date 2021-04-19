---
description: Set 方法會設定指定音訊裝置屬性的值。
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'ITAudioDeviceControl：： Set 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981107"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="fde4b-103">ITAudioDeviceControl：： Set 方法</span><span class="sxs-lookup"><span data-stu-id="fde4b-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="fde4b-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fde4b-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fde4b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fde4b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fde4b-106">**Set** 方法會設定指定 [**音訊裝置屬性**](audiodeviceproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="fde4b-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fde4b-107">語法</span><span class="sxs-lookup"><span data-stu-id="fde4b-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="fde4b-108">參數</span><span class="sxs-lookup"><span data-stu-id="fde4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde4b-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fde4b-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde4b-110">[**AudioDeviceProperty**](audiodeviceproperty.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="fde4b-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="fde4b-111">*左* \[ 值在\]</span><span class="sxs-lookup"><span data-stu-id="fde4b-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde4b-112">屬性所需的值。</span><span class="sxs-lookup"><span data-stu-id="fde4b-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="fde4b-113">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fde4b-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde4b-114">[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出要如何控制 *屬性* 值。</span><span class="sxs-lookup"><span data-stu-id="fde4b-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde4b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fde4b-115">Return value</span></span>

<span data-ttu-id="fde4b-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fde4b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fde4b-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fde4b-117">Return code</span></span>                                                                                   | <span data-ttu-id="fde4b-118">Description</span><span class="sxs-lookup"><span data-stu-id="fde4b-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fde4b-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fde4b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fde4b-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="fde4b-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fde4b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fde4b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fde4b-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="fde4b-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fde4b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fde4b-123">Requirements</span></span>



| <span data-ttu-id="fde4b-124">需求</span><span class="sxs-lookup"><span data-stu-id="fde4b-124">Requirement</span></span> | <span data-ttu-id="fde4b-125">值</span><span class="sxs-lookup"><span data-stu-id="fde4b-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fde4b-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fde4b-126">TAPI version</span></span><br/> | <span data-ttu-id="fde4b-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="fde4b-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="fde4b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fde4b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="fde4b-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fde4b-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fde4b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="fde4b-130">Library</span></span><br/>      | <dl> <span data-ttu-id="fde4b-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="fde4b-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="fde4b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fde4b-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="fde4b-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde4b-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde4b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fde4b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde4b-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="fde4b-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="fde4b-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="fde4b-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="fde4b-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="fde4b-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




