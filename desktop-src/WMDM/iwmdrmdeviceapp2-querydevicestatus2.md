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
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>IWMDRMDeviceApp2：： QueryDeviceStatus2 方法

**QueryDeviceStatus2** 方法會查詢裝置以取得特定的 DRM 狀態或功能。

## <a name="syntax"></a>語法


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

下列其中一個或多個 **DWORD** 值，可指定要要求的功能，並與位 **or** 合併。



| 旗標                              | 描述                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| WMDRM \_ 查詢 \_ 用戶端 \_ INDIVSTATUS | 查詢電腦的 DRM 元件是否需要個人化。       |
| WMDRM \_ 查詢 \_ 裝置 \_ CLOCKSTATUS | 查詢裝置的安全時鐘是否需要新增或更新。        |
| WMDRM \_ 查詢 \_ 裝置 \_ ISREVOKED   | 查詢裝置是否已撤銷。                                         |
| WMDRM \_ 查詢 \_ 裝置 \_ ISWMDRM     | 查詢裝置是否支援適用于可攜式裝置的 Windows Media DRM 10。 |



 

</dd> <dt>

*pdwStatus* \[擴展\]
</dt> <dd>

下列任何一個 **DWORD** 值的零或多個，指定要求的裝置狀態，並與位 **or** 合併。



| 狀態                      | 描述                                              |
|-----------------------------|----------------------------------------------------------|
| WMDRM \_ 裝置 \_ ISWMDRM      | 裝置支援 Windows Media DRM。                   |
| WMDRM \_ 裝置 \_ NEEDCLOCK    | 裝置沒有安全的時鐘。                 |
| 已 \_ 撤銷 WMDRM 裝置 \_      | 裝置已遭撤銷。                             |
| WMDRM \_ 用戶端 \_ NEEDINDIV    | 電腦的 DRM 元件需要個人化。 |
| WMDRM \_ 裝置 \_ REFRESHCLOCK | 時鐘必須重新整理。                         |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                              | Description                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                     | 此方法已成功。<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | 一或多個引數無效。<br/>                           |
| <dl> <dt>**NS \_ E \_ DRM \_ 無效 \_ 憑證**</dt> </dl>          | 從裝置取出的裝置憑證無效。<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 裝置 \_ 憑證**</dt> </dl> | 無法從裝置取得裝置憑證。<br/>     |



 

## <a name="remarks"></a>備註

在對 DRM 內容執行任何受限制的動作之前，應該先呼叫這個方法，例如將 DRM 內容傳送到裝置，或取得計量資訊。 如果 *pdwStatus* 抓取的值表示需要執行某些動作，例如桌上型電腦的 (，或取得裝置) 的時鐘，則應用程式應該呼叫 [**IWMDRMDeviceApp：： AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) ，並將從這個函式取出的 *pdwStatus* 值傳入 **dwFlags** 中的 *AcquireDeviceData* 參數。 如果傳回零，裝置不支援可攜式裝置的 Windows Media DRM 10，且不需要採取任何動作。 如需詳細資訊，請參閱 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl>                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**IWMDRMDeviceApp2 介面**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





