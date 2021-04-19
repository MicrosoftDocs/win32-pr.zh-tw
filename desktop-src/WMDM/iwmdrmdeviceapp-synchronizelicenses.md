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
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>IWMDRMDeviceApp：： SynchronizeLicenses 方法

**SynchronizeLicenses** 方法會在裝置即將過期時，更新該裝置上的授權。

## <a name="syntax"></a>語法


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。

</dd> <dt>

*pProgressCallback* \[在\]
</dt> <dd>

進度回呼，會接收可能需要執行的任何步驟進度。此步驟是透過呼叫之 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)方法的 *EventId* 參數來識別。

</dd> <dt>

*cMinCountThreshold* \[在\]
</dt> <dd>

選用裝置授權的最小剩餘播放次數。

</dd> <dt>

*cMinHoursThreshold* \[在\]
</dt> <dd>

選用裝置授權的剩餘時數下限。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                         | Description                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                | 此方法已成功。<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | 一或多個引數無效。<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | XML 格式不正確。<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ >NOTIMPL**</dt> </dl>                      | 目前未執行這項功能。  (SyncLicenses w/ *pDevice* = Null) <br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | 授權 XML 的格式不正確。<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | 授權 XML 的格式不正確。<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OUTOFMEMORY**</dt> </dl>                  | 記憶體不足。<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | 在授權中找不到必要的 XML 標記。<br/>                                                                                                |
| <dl> <dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt> </dl>    | 指定的裝置不是 Windows Media DRM 相容裝置。<br/>                                                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ 需要有 \_ 個人化**</dt> </dl> | DRM 需要個別的黑色方塊來執行此功能。 換句話說，Windows Media Format SDK 需要安全性升級。<br/> |



 

## <a name="remarks"></a>備註

此呼叫只能在支援可攜式裝置之 Windows Media DRM 10 的裝置上進行。 您必須指定至少一個閾值參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl>                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMProgress3 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp 介面**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





