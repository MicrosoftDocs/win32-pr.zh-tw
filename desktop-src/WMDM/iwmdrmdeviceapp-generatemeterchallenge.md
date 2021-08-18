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
ms.openlocfilehash: e91ac5049740d360ae0c5f53959b3d952188bfa2a569c58a9e7cf86ae0c22577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584547"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>IWMDRMDeviceApp：： GenerateMeterChallenge 方法

**GenerateMeterChallenge** 方法會從裝置取得計量資料。

## <a name="syntax"></a>語法


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)介面的指標。 如果應用程式傳入 **Null**，則會使用儲存在電腦上的計量資訊，而不是來自連線裝置的計量資訊。

</dd> <dt>

*bstrMeterCert* \[在\]
</dt> <dd>

應用程式的計量憑證，作為 **BSTR**。 這是從 Microsoft 收到的已簽署憑證。

</dd> <dt>

*pbstrMeterURL* \[擴展\]
</dt> <dd>

應將計量資料傳送至其中的 URL。 這是由 Windows 媒體裝置管理員所配置，且必須由呼叫者使用 **SysFreeString** 來釋放。

</dd> <dt>

*pbstrMeterData* \[擴展\]
</dt> <dd>

要傳送至計量服務的計量資料。 這是由 Windows 媒體裝置管理員所配置，且必須由呼叫者使用 **SysFreeString** 來釋放。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                      | 描述                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                             | 此方法已成功。<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | 一或多個引數無效。<br/>                               |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>             | XML 格式不正確。<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>             | XML 格式不正確。<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>              | XML 格式不正確。<br/>                                          |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>               | 找不到必要的 XML 標記。<br/>                                 |
| <dl> <dt>**裝置的錯誤**</dt> </dl>            | 有許多裝置錯誤。<br/>                                  |
| <dl> <dt>**DRM 用戶端的錯誤**</dt> </dl>        | 許多內部 DRM 用戶端錯誤。<br/>                     |
| <dl> <dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt> </dl> | 指定的裝置不是 Windows 媒體 DRM 相容裝置。<br/> |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，應用程式應該呼叫 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) 或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) 來確認裝置的所有 DRM 元件都是最新的。 此方法只能在支援可攜式裝置 Windows 媒體 DRM 10 的裝置上呼叫。

已抓取的資料 *pbstrMeterData* 應該傳送至 *pbstrMeterURL* 所指定的 URL。 請務必對抓取的資料進行 URL 編碼，讓它不會在傳輸期間進行修改。

如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。

## <a name="examples"></a>範例

下列 c + + 程式碼範例會建立 **WMDRMDeviceApp** 物件、確認裝置是 Windows 媒體 DRM 10 裝置、其時鐘是否正確，然後要求計量資料。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl>                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDRMDeviceApp 介面**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





