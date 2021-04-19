---
title: 'IWMDRMDeviceApp GenerateMeterChallenge 方法 (WMDRMDeviceApp .h) '
description: GenerateMeterChallenge 方法會從裝置取得計量資料。
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- GenerateMeterChallenge 方法 windows Media 裝置管理員
- GenerateMeterChallenge 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，GenerateMeterChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987115"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="891ce-106">IWMDRMDeviceApp：： GenerateMeterChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="891ce-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="891ce-107">**GenerateMeterChallenge** 方法會從裝置取得計量資料。</span><span class="sxs-lookup"><span data-stu-id="891ce-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="891ce-108">語法</span><span class="sxs-lookup"><span data-stu-id="891ce-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="891ce-109">參數</span><span class="sxs-lookup"><span data-stu-id="891ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891ce-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="891ce-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="891ce-111">[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="891ce-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="891ce-112">如果應用程式傳入 **Null**，則會使用儲存在電腦上的計量資訊，而不是來自連線裝置的計量資訊。</span><span class="sxs-lookup"><span data-stu-id="891ce-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="891ce-113">*bstrMeterCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="891ce-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="891ce-114">應用程式的計量憑證，作為 **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="891ce-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="891ce-115">這是從 Microsoft 收到的已簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="891ce-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="891ce-116">*pbstrMeterURL* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="891ce-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="891ce-117">應將計量資料傳送至其中的 URL。</span><span class="sxs-lookup"><span data-stu-id="891ce-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="891ce-118">這是由 Windows Media 裝置管理員所配置，且必須由呼叫端使用 **SysFreeString** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="891ce-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="891ce-119">*pbstrMeterData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="891ce-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="891ce-120">要傳送至計量服務的計量資料。</span><span class="sxs-lookup"><span data-stu-id="891ce-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="891ce-121">這是由 Windows Media 裝置管理員所配置，且必須由呼叫端使用 **SysFreeString** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="891ce-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891ce-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="891ce-122">Return value</span></span>

<span data-ttu-id="891ce-123">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="891ce-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="891ce-124">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="891ce-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="891ce-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="891ce-125">Return code</span></span>                                                                                                      | <span data-ttu-id="891ce-126">Description</span><span class="sxs-lookup"><span data-stu-id="891ce-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="891ce-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="891ce-128">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="891ce-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="891ce-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="891ce-130">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="891ce-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="891ce-131"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="891ce-132">XML 格式不正確。</span><span class="sxs-lookup"><span data-stu-id="891ce-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="891ce-133"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="891ce-134">XML 格式不正確。</span><span class="sxs-lookup"><span data-stu-id="891ce-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="891ce-135"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="891ce-136">XML 格式不正確。</span><span class="sxs-lookup"><span data-stu-id="891ce-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="891ce-137"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="891ce-138">找不到必要的 XML 標記。</span><span class="sxs-lookup"><span data-stu-id="891ce-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="891ce-139"><dt>**裝置的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="891ce-140">有許多裝置錯誤。</span><span class="sxs-lookup"><span data-stu-id="891ce-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="891ce-141"><dt>**DRM 用戶端的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="891ce-142">許多內部 DRM 用戶端錯誤。</span><span class="sxs-lookup"><span data-stu-id="891ce-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="891ce-143"><dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="891ce-144">指定的裝置不是 Windows Media DRM 相容裝置。</span><span class="sxs-lookup"><span data-stu-id="891ce-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="891ce-145">備註</span><span class="sxs-lookup"><span data-stu-id="891ce-145">Remarks</span></span>

<span data-ttu-id="891ce-146">在呼叫這個方法之前，應用程式應該呼叫 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) 或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) 來確認裝置的所有 DRM 元件都是最新的。</span><span class="sxs-lookup"><span data-stu-id="891ce-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="891ce-147">此方法只能在支援可攜式裝置之 Windows Media DRM 10 的裝置上呼叫。</span><span class="sxs-lookup"><span data-stu-id="891ce-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="891ce-148">已抓取的資料 *pbstrMeterData* 應該傳送至 *pbstrMeterURL* 所指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="891ce-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="891ce-149">請務必對抓取的資料進行 URL 編碼，讓它不會在傳輸期間進行修改。</span><span class="sxs-lookup"><span data-stu-id="891ce-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="891ce-150">如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。</span><span class="sxs-lookup"><span data-stu-id="891ce-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="891ce-151">範例</span><span class="sxs-lookup"><span data-stu-id="891ce-151">Examples</span></span>

<span data-ttu-id="891ce-152">下列 c + + 程式碼範例會建立 **WMDRMDeviceApp** 物件、確認裝置是 WINDOWS Media DRM 10 裝置、其時鐘是否正確，然後要求計量資料。</span><span class="sxs-lookup"><span data-stu-id="891ce-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="891ce-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="891ce-153">Requirements</span></span>



| <span data-ttu-id="891ce-154">需求</span><span class="sxs-lookup"><span data-stu-id="891ce-154">Requirement</span></span> | <span data-ttu-id="891ce-155">值</span><span class="sxs-lookup"><span data-stu-id="891ce-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891ce-156">標頭</span><span class="sxs-lookup"><span data-stu-id="891ce-156">Header</span></span><br/>  | <dl> <span data-ttu-id="891ce-157"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="891ce-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="891ce-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="891ce-158">Library</span></span><br/> | <dl> <span data-ttu-id="891ce-159"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="891ce-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="891ce-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="891ce-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891ce-161">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="891ce-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="891ce-162">**IWMDMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="891ce-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="891ce-163">**IWMDRMDeviceApp 介面**</span><span class="sxs-lookup"><span data-stu-id="891ce-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





