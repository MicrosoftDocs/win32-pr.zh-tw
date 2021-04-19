---
title: 'IWMDRMDeviceApp2 QueryDeviceStatus2 方法 (WMDRMDeviceApp .h) '
description: QueryDeviceStatus2 方法會查詢裝置以取得特定的 DRM 狀態或功能。
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- QueryDeviceStatus2 方法 windows Media 裝置管理員
- QueryDeviceStatus2 方法 windows Media 裝置管理員，IWMDRMDeviceApp2 介面
- IWMDRMDeviceApp2 interface windows Media 裝置管理員，QueryDeviceStatus2 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990260"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="928c4-106">IWMDRMDeviceApp2：： QueryDeviceStatus2 方法</span><span class="sxs-lookup"><span data-stu-id="928c4-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="928c4-107">**QueryDeviceStatus2** 方法會查詢裝置以取得特定的 DRM 狀態或功能。</span><span class="sxs-lookup"><span data-stu-id="928c4-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="928c4-108">語法</span><span class="sxs-lookup"><span data-stu-id="928c4-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="928c4-109">參數</span><span class="sxs-lookup"><span data-stu-id="928c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928c4-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="928c4-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928c4-111">[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="928c4-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="928c4-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="928c4-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928c4-113">下列其中一個或多個 **DWORD** 值，可指定要要求的功能，並與位 **or** 合併。</span><span class="sxs-lookup"><span data-stu-id="928c4-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="928c4-114">旗標</span><span class="sxs-lookup"><span data-stu-id="928c4-114">Flag</span></span>                              | <span data-ttu-id="928c4-115">描述</span><span class="sxs-lookup"><span data-stu-id="928c4-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="928c4-116">WMDRM \_ 查詢 \_ 用戶端 \_ INDIVSTATUS</span><span class="sxs-lookup"><span data-stu-id="928c4-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="928c4-117">查詢電腦的 DRM 元件是否需要個人化。</span><span class="sxs-lookup"><span data-stu-id="928c4-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="928c4-118">WMDRM \_ 查詢 \_ 裝置 \_ CLOCKSTATUS</span><span class="sxs-lookup"><span data-stu-id="928c4-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="928c4-119">查詢裝置的安全時鐘是否需要新增或更新。</span><span class="sxs-lookup"><span data-stu-id="928c4-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="928c4-120">WMDRM \_ 查詢 \_ 裝置 \_ ISREVOKED</span><span class="sxs-lookup"><span data-stu-id="928c4-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="928c4-121">查詢裝置是否已撤銷。</span><span class="sxs-lookup"><span data-stu-id="928c4-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="928c4-122">WMDRM \_ 查詢 \_ 裝置 \_ ISWMDRM</span><span class="sxs-lookup"><span data-stu-id="928c4-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="928c4-123">查詢裝置是否支援適用于可攜式裝置的 Windows Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="928c4-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="928c4-124">*pdwStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="928c4-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="928c4-125">下列任何一個 **DWORD** 值的零或多個，指定要求的裝置狀態，並與位 **or** 合併。</span><span class="sxs-lookup"><span data-stu-id="928c4-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="928c4-126">狀態</span><span class="sxs-lookup"><span data-stu-id="928c4-126">Status</span></span>                      | <span data-ttu-id="928c4-127">描述</span><span class="sxs-lookup"><span data-stu-id="928c4-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="928c4-128">WMDRM \_ 裝置 \_ ISWMDRM</span><span class="sxs-lookup"><span data-stu-id="928c4-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="928c4-129">裝置支援 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="928c4-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="928c4-130">WMDRM \_ 裝置 \_ NEEDCLOCK</span><span class="sxs-lookup"><span data-stu-id="928c4-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="928c4-131">裝置沒有安全的時鐘。</span><span class="sxs-lookup"><span data-stu-id="928c4-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="928c4-132">已 \_ 撤銷 WMDRM 裝置 \_</span><span class="sxs-lookup"><span data-stu-id="928c4-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="928c4-133">裝置已遭撤銷。</span><span class="sxs-lookup"><span data-stu-id="928c4-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="928c4-134">WMDRM \_ 用戶端 \_ NEEDINDIV</span><span class="sxs-lookup"><span data-stu-id="928c4-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="928c4-135">電腦的 DRM 元件需要個人化。</span><span class="sxs-lookup"><span data-stu-id="928c4-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="928c4-136">WMDRM \_ 裝置 \_ REFRESHCLOCK</span><span class="sxs-lookup"><span data-stu-id="928c4-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="928c4-137">時鐘必須重新整理。</span><span class="sxs-lookup"><span data-stu-id="928c4-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928c4-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="928c4-138">Return value</span></span>

<span data-ttu-id="928c4-139">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="928c4-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="928c4-140">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="928c4-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="928c4-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="928c4-141">Return code</span></span>                                                                                                              | <span data-ttu-id="928c4-142">Description</span><span class="sxs-lookup"><span data-stu-id="928c4-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="928c4-143"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="928c4-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="928c4-144">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="928c4-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="928c4-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="928c4-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="928c4-146">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="928c4-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="928c4-147"><dt>**NS \_ E \_ DRM \_ 無效 \_ 憑證**</dt></span><span class="sxs-lookup"><span data-stu-id="928c4-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="928c4-148">從裝置取出的裝置憑證無效。</span><span class="sxs-lookup"><span data-stu-id="928c4-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="928c4-149"><dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 裝置 \_ 憑證**</dt></span><span class="sxs-lookup"><span data-stu-id="928c4-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="928c4-150">無法從裝置取得裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="928c4-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="928c4-151">備註</span><span class="sxs-lookup"><span data-stu-id="928c4-151">Remarks</span></span>

<span data-ttu-id="928c4-152">在對 DRM 內容執行任何受限制的動作之前，應該先呼叫這個方法，例如將 DRM 內容傳送到裝置，或取得計量資訊。</span><span class="sxs-lookup"><span data-stu-id="928c4-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="928c4-153">如果 *pdwStatus* 抓取的值表示需要執行某些動作，例如桌上型電腦的 (，或取得裝置) 的時鐘，則應用程式應該呼叫 [**IWMDRMDeviceApp：： AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) ，並將從這個函式取出的 *pdwStatus* 值傳入 **dwFlags** 中的 *AcquireDeviceData* 參數。</span><span class="sxs-lookup"><span data-stu-id="928c4-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="928c4-154">如果傳回零，裝置不支援可攜式裝置的 Windows Media DRM 10，且不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="928c4-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="928c4-155">如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。</span><span class="sxs-lookup"><span data-stu-id="928c4-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="928c4-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="928c4-156">Requirements</span></span>



| <span data-ttu-id="928c4-157">需求</span><span class="sxs-lookup"><span data-stu-id="928c4-157">Requirement</span></span> | <span data-ttu-id="928c4-158">值</span><span class="sxs-lookup"><span data-stu-id="928c4-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="928c4-159">標頭</span><span class="sxs-lookup"><span data-stu-id="928c4-159">Header</span></span><br/>  | <dl> <span data-ttu-id="928c4-160"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="928c4-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="928c4-161">程式庫</span><span class="sxs-lookup"><span data-stu-id="928c4-161">Library</span></span><br/> | <dl> <span data-ttu-id="928c4-162"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="928c4-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="928c4-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="928c4-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928c4-164">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="928c4-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="928c4-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="928c4-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="928c4-166">**IWMDRMDeviceApp2 介面**</span><span class="sxs-lookup"><span data-stu-id="928c4-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





