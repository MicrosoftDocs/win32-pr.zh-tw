---
title: 'IWMDRMDeviceApp SynchronizeLicenses 方法 (WMDRMDeviceApp .h) '
description: SynchronizeLicenses 方法會在裝置即將過期時，更新該裝置上的授權。
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- SynchronizeLicenses 方法 windows Media 裝置管理員
- SynchronizeLicenses 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，SynchronizeLicenses 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977566"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="8ac3a-106">IWMDRMDeviceApp：： SynchronizeLicenses 方法</span><span class="sxs-lookup"><span data-stu-id="8ac3a-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="8ac3a-107">**SynchronizeLicenses** 方法會在裝置即將過期時，更新該裝置上的授權。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac3a-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ac3a-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="8ac3a-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ac3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac3a-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ac3a-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac3a-111">[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="8ac3a-112">*pProgressCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ac3a-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac3a-113">進度回呼，會接收可能需要執行的任何步驟進度。此步驟是透過呼叫之 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)方法的 *EventId* 參數來識別。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="8ac3a-114">*cMinCountThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ac3a-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac3a-115">選用裝置授權的最小剩餘播放次數。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="8ac3a-116">*cMinHoursThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ac3a-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac3a-117">選用裝置授權的剩餘時數下限。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac3a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ac3a-118">Return value</span></span>

<span data-ttu-id="8ac3a-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ac3a-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ac3a-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8ac3a-121">Return code</span></span>                                                                                                         | <span data-ttu-id="8ac3a-122">Description</span><span class="sxs-lookup"><span data-stu-id="8ac3a-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ac3a-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="8ac3a-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="8ac3a-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="8ac3a-126">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="8ac3a-127"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="8ac3a-128">XML 格式不正確。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="8ac3a-129"><dt>**DRM \_ E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="8ac3a-130">目前未執行這項功能。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="8ac3a-131"> (SyncLicenses w/ *pDevice* = Null) </span><span class="sxs-lookup"><span data-stu-id="8ac3a-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="8ac3a-132"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="8ac3a-133">授權 XML 的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="8ac3a-134"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="8ac3a-135">授權 XML 的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="8ac3a-136"><dt>**DRM \_ E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="8ac3a-137">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="8ac3a-138"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="8ac3a-139">在授權中找不到必要的 XML 標記。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="8ac3a-140"><dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="8ac3a-141">指定的裝置不是 Windows Media DRM 相容裝置。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="8ac3a-142"><dt>**NS \_ E \_ DRM \_ 需要有 \_ 個人化**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="8ac3a-143">DRM 需要個別的黑色方塊來執行此功能。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="8ac3a-144">換句話說，Windows Media Format SDK 需要安全性升級。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ac3a-145">備註</span><span class="sxs-lookup"><span data-stu-id="8ac3a-145">Remarks</span></span>

<span data-ttu-id="8ac3a-146">此呼叫只能在支援可攜式裝置之 Windows Media DRM 10 的裝置上進行。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="8ac3a-147">您必須指定至少一個閾值參數。</span><span class="sxs-lookup"><span data-stu-id="8ac3a-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac3a-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ac3a-148">Requirements</span></span>



| <span data-ttu-id="8ac3a-149">需求</span><span class="sxs-lookup"><span data-stu-id="8ac3a-149">Requirement</span></span> | <span data-ttu-id="8ac3a-150">值</span><span class="sxs-lookup"><span data-stu-id="8ac3a-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac3a-151">標頭</span><span class="sxs-lookup"><span data-stu-id="8ac3a-151">Header</span></span><br/>  | <dl> <span data-ttu-id="8ac3a-152"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="8ac3a-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ac3a-153">Library</span></span><br/> | <dl> <span data-ttu-id="8ac3a-154"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ac3a-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="8ac3a-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ac3a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac3a-156">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="8ac3a-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="8ac3a-157">**IWMDMProgress3 介面**</span><span class="sxs-lookup"><span data-stu-id="8ac3a-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="8ac3a-158">**IWMDRMDeviceApp 介面**</span><span class="sxs-lookup"><span data-stu-id="8ac3a-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





