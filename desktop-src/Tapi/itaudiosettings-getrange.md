---
description: GetRange 方法會抓取指定音訊設定屬性的有效值範圍。
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'ITAudioSettings：： GetRange 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001545"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="82cbb-103">ITAudioSettings：： GetRange 方法</span><span class="sxs-lookup"><span data-stu-id="82cbb-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="82cbb-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="82cbb-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82cbb-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="82cbb-106">**GetRange** 方法會抓取指定 [**音訊設定屬性**](audiosettingsproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="82cbb-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82cbb-107">語法</span><span class="sxs-lookup"><span data-stu-id="82cbb-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="82cbb-108">參數</span><span class="sxs-lookup"><span data-stu-id="82cbb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82cbb-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-110">[**AudioSettingsProperty**](audiosettingsproperty.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="82cbb-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="82cbb-111">*plMin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-112">輸入屬性的最小有效值。</span><span class="sxs-lookup"><span data-stu-id="82cbb-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="82cbb-113">*plMax* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-114">輸入屬性的最大有效值。</span><span class="sxs-lookup"><span data-stu-id="82cbb-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="82cbb-115">*plSteppingDelta* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-116">可以增加或減少屬性值的遞增量。</span><span class="sxs-lookup"><span data-stu-id="82cbb-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="82cbb-117">*plDefault* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-118">*Property* 參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="82cbb-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="82cbb-119">*plFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82cbb-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82cbb-120">[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出 *屬性* 值的控制方式。</span><span class="sxs-lookup"><span data-stu-id="82cbb-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82cbb-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="82cbb-121">Return value</span></span>

<span data-ttu-id="82cbb-122">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="82cbb-122">This method can return one of these values.</span></span>



| <span data-ttu-id="82cbb-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="82cbb-123">Return code</span></span>                                                                                   | <span data-ttu-id="82cbb-124">Description</span><span class="sxs-lookup"><span data-stu-id="82cbb-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="82cbb-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="82cbb-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82cbb-126">方法成功。</span><span class="sxs-lookup"><span data-stu-id="82cbb-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="82cbb-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82cbb-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82cbb-128">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="82cbb-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="82cbb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="82cbb-129">Requirements</span></span>



| <span data-ttu-id="82cbb-130">需求</span><span class="sxs-lookup"><span data-stu-id="82cbb-130">Requirement</span></span> | <span data-ttu-id="82cbb-131">值</span><span class="sxs-lookup"><span data-stu-id="82cbb-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82cbb-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="82cbb-132">TAPI version</span></span><br/> | <span data-ttu-id="82cbb-133">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="82cbb-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="82cbb-134">標頭</span><span class="sxs-lookup"><span data-stu-id="82cbb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="82cbb-135"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="82cbb-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="82cbb-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="82cbb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="82cbb-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="82cbb-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="82cbb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="82cbb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="82cbb-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82cbb-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cbb-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82cbb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cbb-141">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="82cbb-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="82cbb-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="82cbb-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="82cbb-143">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="82cbb-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




