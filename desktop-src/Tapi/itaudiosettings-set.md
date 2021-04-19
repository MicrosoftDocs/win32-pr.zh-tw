---
description: Set 方法會設定指定之音訊設定屬性的值。
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'ITAudioSettings：： Set 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995437"
---
# <a name="itaudiosettingsset-method"></a><span data-ttu-id="700a3-103">ITAudioSettings：： Set 方法</span><span class="sxs-lookup"><span data-stu-id="700a3-103">ITAudioSettings::Set method</span></span>

<span data-ttu-id="700a3-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="700a3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="700a3-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="700a3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="700a3-106">**Set** 方法會設定指定之 [**音訊設定屬性**](audiosettingsproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="700a3-106">The **Set** method sets the value of a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="700a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="700a3-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="700a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="700a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700a3-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="700a3-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700a3-110">[**AudioSettingsProperty**](audiosettingsproperty.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="700a3-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="700a3-111">*左* \[ 值在\]</span><span class="sxs-lookup"><span data-stu-id="700a3-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700a3-112">屬性所需的值。</span><span class="sxs-lookup"><span data-stu-id="700a3-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="700a3-113">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="700a3-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700a3-114">[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出要如何控制 *屬性* 值。</span><span class="sxs-lookup"><span data-stu-id="700a3-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700a3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="700a3-115">Return value</span></span>

<span data-ttu-id="700a3-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="700a3-116">This method can return one of these values.</span></span>



| <span data-ttu-id="700a3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="700a3-117">Return code</span></span>                                                                                   | <span data-ttu-id="700a3-118">Description</span><span class="sxs-lookup"><span data-stu-id="700a3-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="700a3-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="700a3-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="700a3-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="700a3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="700a3-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="700a3-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="700a3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="700a3-123">Requirements</span></span>



| <span data-ttu-id="700a3-124">需求</span><span class="sxs-lookup"><span data-stu-id="700a3-124">Requirement</span></span> | <span data-ttu-id="700a3-125">值</span><span class="sxs-lookup"><span data-stu-id="700a3-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="700a3-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="700a3-126">TAPI version</span></span><br/> | <span data-ttu-id="700a3-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="700a3-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="700a3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="700a3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="700a3-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="700a3-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="700a3-130">Library</span></span><br/>      | <dl> <span data-ttu-id="700a3-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="700a3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="700a3-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="700a3-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="700a3-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700a3-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="700a3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700a3-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="700a3-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="700a3-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="700a3-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="700a3-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="700a3-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




