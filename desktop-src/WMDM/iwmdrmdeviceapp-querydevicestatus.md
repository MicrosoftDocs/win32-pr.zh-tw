---
title: 'IWMDRMDeviceApp QueryDeviceStatus 方法 (WMDRMDeviceApp .h) '
description: QueryDeviceStatus 方法會查詢裝置的目前 DRM 狀態和功能。
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- QueryDeviceStatus 方法 windows Media 裝置管理員
- QueryDeviceStatus 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，QueryDeviceStatus 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990054"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="0a565-106">IWMDRMDeviceApp：： QueryDeviceStatus 方法</span><span class="sxs-lookup"><span data-stu-id="0a565-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="0a565-107">**QueryDeviceStatus** 方法會查詢裝置的目前 DRM 狀態和功能。</span><span class="sxs-lookup"><span data-stu-id="0a565-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a565-108">語法</span><span class="sxs-lookup"><span data-stu-id="0a565-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="0a565-109">參數</span><span class="sxs-lookup"><span data-stu-id="0a565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a565-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a565-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a565-111">[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0a565-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="0a565-112">*pdwStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a565-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a565-113">下列 **DWORD** 值的零或多個會描述裝置的 DRM 部分，並與位 **or** 結合。</span><span class="sxs-lookup"><span data-stu-id="0a565-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="0a565-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0a565-114">See Remarks.</span></span>



| <span data-ttu-id="0a565-115">狀態</span><span class="sxs-lookup"><span data-stu-id="0a565-115">Status</span></span>                      | <span data-ttu-id="0a565-116">描述</span><span class="sxs-lookup"><span data-stu-id="0a565-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="0a565-117">WMDRM \_ 裝置 \_ ISWMDRM</span><span class="sxs-lookup"><span data-stu-id="0a565-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="0a565-118">裝置支援 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="0a565-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="0a565-119">WMDRM \_ 裝置 \_ NEEDCLOCK</span><span class="sxs-lookup"><span data-stu-id="0a565-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="0a565-120">裝置沒有安全的時鐘。</span><span class="sxs-lookup"><span data-stu-id="0a565-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="0a565-121">已 \_ 撤銷 WMDRM 裝置 \_</span><span class="sxs-lookup"><span data-stu-id="0a565-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="0a565-122">裝置已遭撤銷。</span><span class="sxs-lookup"><span data-stu-id="0a565-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="0a565-123">WMDRM \_ 用戶端 \_ NEEDINDIV</span><span class="sxs-lookup"><span data-stu-id="0a565-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="0a565-124">DRM 安全性需要個人化。</span><span class="sxs-lookup"><span data-stu-id="0a565-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="0a565-125">WMDRM \_ 裝置 \_ REFRESHCLOCK</span><span class="sxs-lookup"><span data-stu-id="0a565-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="0a565-126">時鐘必須重新整理。</span><span class="sxs-lookup"><span data-stu-id="0a565-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a565-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a565-127">Return value</span></span>

<span data-ttu-id="0a565-128">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0a565-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0a565-129">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0a565-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0a565-130">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0a565-130">Return code</span></span>                                                                                                              | <span data-ttu-id="0a565-131">Description</span><span class="sxs-lookup"><span data-stu-id="0a565-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a565-132"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0a565-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="0a565-133">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0a565-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0a565-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a565-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="0a565-135">輸入引數無效。</span><span class="sxs-lookup"><span data-stu-id="0a565-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="0a565-136"><dt>**NS \_ E \_ DRM \_ 無效 \_ 憑證**</dt></span><span class="sxs-lookup"><span data-stu-id="0a565-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="0a565-137">從裝置取出的裝置憑證無效。</span><span class="sxs-lookup"><span data-stu-id="0a565-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0a565-138"><dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 裝置 \_ 憑證**</dt></span><span class="sxs-lookup"><span data-stu-id="0a565-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="0a565-139">無法從裝置取得裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="0a565-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0a565-140">備註</span><span class="sxs-lookup"><span data-stu-id="0a565-140">Remarks</span></span>

<span data-ttu-id="0a565-141">在對 DRM 內容執行任何受限制的動作之前，應該先呼叫這個方法，例如將 DRM 內容傳送到裝置，或取得計量資訊。</span><span class="sxs-lookup"><span data-stu-id="0a565-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="0a565-142">如果 *pdwStatus* 所抓取的值表示需要執行某些動作，例如桌上型電腦的 (，或取得裝置) 的時鐘，則應用程式應該呼叫 [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) ，並將從這個函式取出的 *pdwStatus* 值傳遞給 **AcquireDeviceData** 中的 *dwFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="0a565-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="0a565-143">如果傳回零，裝置不支援可攜式裝置的 Windows Media DRM 10，且不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="0a565-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="0a565-144">如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a565-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="0a565-145">範例</span><span class="sxs-lookup"><span data-stu-id="0a565-145">Examples</span></span>

<span data-ttu-id="0a565-146">下列 c + + 程式碼範例會建立 **WMDRMDeviceApp** 物件、確認裝置是 WINDOWS Media DRM 10 裝置、其時鐘是否正確，然後要求計量資料。</span><span class="sxs-lookup"><span data-stu-id="0a565-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="0a565-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a565-147">Requirements</span></span>



| <span data-ttu-id="0a565-148">需求</span><span class="sxs-lookup"><span data-stu-id="0a565-148">Requirement</span></span> | <span data-ttu-id="0a565-149">值</span><span class="sxs-lookup"><span data-stu-id="0a565-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a565-150">標頭</span><span class="sxs-lookup"><span data-stu-id="0a565-150">Header</span></span><br/>  | <dl> <span data-ttu-id="0a565-151"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="0a565-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="0a565-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a565-152">Library</span></span><br/> | <dl> <span data-ttu-id="0a565-153"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a565-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="0a565-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a565-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a565-155">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="0a565-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="0a565-156">**IWMDRMDeviceApp 介面**</span><span class="sxs-lookup"><span data-stu-id="0a565-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="0a565-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="0a565-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





