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
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>IWMDRMDeviceApp：： QueryDeviceStatus 方法

**QueryDeviceStatus** 方法會查詢裝置的目前 DRM 狀態和功能。

## <a name="syntax"></a>語法


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。

</dd> <dt>

*pdwStatus* \[擴展\]
</dt> <dd>

下列 **DWORD** 值的零或多個會描述裝置的 DRM 部分，並與位 **or** 結合。 請參閱＜備註＞。



| 狀態                      | 描述                                  |
|-----------------------------|----------------------------------------------|
| WMDRM \_ 裝置 \_ ISWMDRM      | 裝置支援 Windows Media DRM。       |
| WMDRM \_ 裝置 \_ NEEDCLOCK    | 裝置沒有安全的時鐘。     |
| 已 \_ 撤銷 WMDRM 裝置 \_      | 裝置已遭撤銷。                 |
| WMDRM \_ 用戶端 \_ NEEDINDIV    | DRM 安全性需要個人化。 |
| WMDRM \_ 裝置 \_ REFRESHCLOCK | 時鐘必須重新整理。             |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                              | Description                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                     | 此方法已成功。<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | 輸入引數無效。<br/>                               |
| <dl> <dt>**NS \_ E \_ DRM \_ 無效 \_ 憑證**</dt> </dl>          | 從裝置取出的裝置憑證無效。<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 裝置 \_ 憑證**</dt> </dl> | 無法從裝置取得裝置憑證。<br/>     |



 

## <a name="remarks"></a>備註

在對 DRM 內容執行任何受限制的動作之前，應該先呼叫這個方法，例如將 DRM 內容傳送到裝置，或取得計量資訊。 如果 *pdwStatus* 所抓取的值表示需要執行某些動作，例如桌上型電腦的 (，或取得裝置) 的時鐘，則應用程式應該呼叫 [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) ，並將從這個函式取出的 *pdwStatus* 值傳遞給 **AcquireDeviceData** 中的 *dwFlags* 參數。 如果傳回零，裝置不支援可攜式裝置的 Windows Media DRM 10，且不需要採取任何動作。 如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。

## <a name="examples"></a>範例

下列 c + + 程式碼範例會建立 **WMDRMDeviceApp** 物件、確認裝置是 WINDOWS Media DRM 10 裝置、其時鐘是否正確，然後要求計量資料。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl>                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp 介面**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





