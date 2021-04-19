---
title: 'IWMDRMDeviceApp AcquireDeviceData 方法 (WMDRMDeviceApp .h) '
description: AcquireDeviceData 方法會初始化或重設裝置安全時鐘。
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- AcquireDeviceData 方法 windows Media 裝置管理員
- AcquireDeviceData 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，AcquireDeviceData 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982603"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="ef612-106">IWMDRMDeviceApp：： AcquireDeviceData 方法</span><span class="sxs-lookup"><span data-stu-id="ef612-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="ef612-107">**AcquireDeviceData** 方法會初始化或重設裝置安全時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef612-108">語法</span><span class="sxs-lookup"><span data-stu-id="ef612-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ef612-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef612-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef612-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef612-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef612-111">將報告計量資料之裝置的 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ef612-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="ef612-112">*pProgressCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef612-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef612-113">進度回呼，應用程式可以透過此回呼來追蹤事件的進度，或取消事件。</span><span class="sxs-lookup"><span data-stu-id="ef612-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="ef612-114">進度是由 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)方法的 *EventId* 參數所識別。</span><span class="sxs-lookup"><span data-stu-id="ef612-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="ef612-115">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef612-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef612-116">下列其中一個或兩個旗標的邏輯 **or** ，指定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="ef612-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="ef612-117">此值會從 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)的 *pdwStatus* 參數中取出。</span><span class="sxs-lookup"><span data-stu-id="ef612-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="ef612-118">您可以直接使用 *pdwStatus* 旗標。</span><span class="sxs-lookup"><span data-stu-id="ef612-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="ef612-119">旗標</span><span class="sxs-lookup"><span data-stu-id="ef612-119">Flag</span></span>                        | <span data-ttu-id="ef612-120">描述</span><span class="sxs-lookup"><span data-stu-id="ef612-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="ef612-121">WMDRM \_ 裝置 \_ NEEDCLOCK</span><span class="sxs-lookup"><span data-stu-id="ef612-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="ef612-122">從安全的時鐘伺服器取得時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="ef612-123">WMDRM \_ 裝置 \_ REFRESHCLOCK</span><span class="sxs-lookup"><span data-stu-id="ef612-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="ef612-124">從安全的時鐘伺服器更新時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ef612-125">*pdwStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef612-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef612-126">下列其中一個 **DWORD** 值，指定裝置所傳回的狀態。</span><span class="sxs-lookup"><span data-stu-id="ef612-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="ef612-127">狀態</span><span class="sxs-lookup"><span data-stu-id="ef612-127">Status</span></span> | <span data-ttu-id="ef612-128">描述</span><span class="sxs-lookup"><span data-stu-id="ef612-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="ef612-129">0</span><span class="sxs-lookup"><span data-stu-id="ef612-129">0</span></span>      | <span data-ttu-id="ef612-130">不支援此動作。</span><span class="sxs-lookup"><span data-stu-id="ef612-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="ef612-131">1</span><span class="sxs-lookup"><span data-stu-id="ef612-131">1</span></span>      | <span data-ttu-id="ef612-132">無法從服務取得裝置安全時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="ef612-133">2</span><span class="sxs-lookup"><span data-stu-id="ef612-133">2</span></span>      | <span data-ttu-id="ef612-134">無法設定裝置的安全時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="ef612-135">3</span><span class="sxs-lookup"><span data-stu-id="ef612-135">3</span></span>      | <span data-ttu-id="ef612-136">裝置的安全時鐘已設定。</span><span class="sxs-lookup"><span data-stu-id="ef612-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef612-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef612-137">Return value</span></span>

<span data-ttu-id="ef612-138">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ef612-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef612-139">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ef612-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef612-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ef612-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="ef612-141">Description</span><span class="sxs-lookup"><span data-stu-id="ef612-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef612-142"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="ef612-143">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ef612-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="ef612-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="ef612-145">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="ef612-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="ef612-146"><dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="ef612-147">指定的裝置不是 Windows Media DRM 相容裝置。</span><span class="sxs-lookup"><span data-stu-id="ef612-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ef612-148"><dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 安全 \_ 時鐘**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="ef612-149">無法從裝置取得安全的時鐘挑戰，或無法從挑戰中取得安全的時鐘 URL。</span><span class="sxs-lookup"><span data-stu-id="ef612-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="ef612-150"><dt>**NS \_ E \_ DRM \_ 無法 \_ \_ \_ \_ \_ 從伺服器取得安全時鐘 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="ef612-151">無法從安全的時鐘伺服器取得安全的時鐘回應。</span><span class="sxs-lookup"><span data-stu-id="ef612-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ef612-152"><dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 設定 \_ 安全 \_ 時鐘**</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="ef612-153">無法將安全時鐘挑戰傳送到裝置，或裝置無法設定時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="ef612-154">備註</span><span class="sxs-lookup"><span data-stu-id="ef612-154">Remarks</span></span>

<span data-ttu-id="ef612-155">這是非同步方法;裝置必須等待此作業的 [**IWMDMProgress：： End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) 回呼，才能嘗試播放任何授權的內容。</span><span class="sxs-lookup"><span data-stu-id="ef612-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="ef612-156">應用程式可以藉由呼叫 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) 或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)，來瞭解裝置是否必須重設或更新時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="ef612-157">您的應用程式必須具有網際網路連線，才能讓它取得或重設安全的時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef612-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef612-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef612-158">Requirements</span></span>



| <span data-ttu-id="ef612-159">需求</span><span class="sxs-lookup"><span data-stu-id="ef612-159">Requirement</span></span> | <span data-ttu-id="ef612-160">值</span><span class="sxs-lookup"><span data-stu-id="ef612-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef612-161">標頭</span><span class="sxs-lookup"><span data-stu-id="ef612-161">Header</span></span><br/>  | <dl> <span data-ttu-id="ef612-162"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="ef612-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="ef612-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef612-163">Library</span></span><br/> | <dl> <span data-ttu-id="ef612-164"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef612-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="ef612-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef612-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef612-166">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="ef612-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="ef612-167">**IWMDMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="ef612-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="ef612-168">**IWMDMProgress3 介面**</span><span class="sxs-lookup"><span data-stu-id="ef612-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="ef612-169">**IWMDRMDeviceApp 介面**</span><span class="sxs-lookup"><span data-stu-id="ef612-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





