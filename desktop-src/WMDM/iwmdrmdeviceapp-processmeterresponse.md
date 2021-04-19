---
title: 'IWMDRMDeviceApp ProcessMeterResponse 方法 (WMDRMDeviceApp .h) '
description: ProcessMeterResponse 方法會重設裝置上的部分或所有計量計數，之後裝置的資料就會由伺服器傳送和處理。
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- ProcessMeterResponse 方法 windows Media 裝置管理員
- ProcessMeterResponse 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，ProcessMeterResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998809"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>IWMDRMDeviceApp：:P rocessMeterResponse 方法

**ProcessMeterResponse** 方法會重設裝置上的部分或所有計量計數，之後裝置的資料就會由伺服器傳送和處理。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。

</dd> <dt>

*pbResponse* \[在\]
</dt> <dd>

傳送使用 [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)產生的資料之後，從計量伺服器收到的回應。

</dd> <dt>

*cbResponse* \[在\]
</dt> <dd>

*PbResponse* 的大小（以位元組為單位）。

</dd> <dt>

*pdwFlags* \[擴展\]
</dt> <dd>

下表中的 **DWORD** ，指出裝置上是否有更多需要處理的計量資料。



| 旗標                            | 描述                                     |
|---------------------------------|-------------------------------------------------|
| WMDRM \_ 計量 \_ 回應 \_ 全部     | 已處理所有計量資料。           |
| WMDRM \_ 計量 \_ 回應 \_ 部分 | 需要處理額外的計量資料。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                      | Description                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                             | 此方法已成功。<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | 一或多個引數無效。<br/>                               |
| <dl> <dt>**裝置的錯誤**</dt> </dl>            | 有許多裝置錯誤。<br/>                                  |
| <dl> <dt>**DRM 用戶端的錯誤**</dt> </dl>        | 許多內部 DRM 用戶端錯誤。<br/>                     |
| <dl> <dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt> </dl> | 指定的裝置不是 Windows Media DRM 相容裝置。<br/> |



 

## <a name="remarks"></a>備註

如需有關計量的詳細資訊（包括程式碼範例），請參閱 MSDN 網站上的 [使用 Windows MEDIA DRM 10 的數位媒體內容的計量](/previous-versions//bb614723(v=vs.85)) 技術白皮書。

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

 

