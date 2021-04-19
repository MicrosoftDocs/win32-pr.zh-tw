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
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>IWMDRMDeviceApp：： AcquireDeviceData 方法

**AcquireDeviceData** 方法會初始化或重設裝置安全時鐘。

## <a name="syntax"></a>語法


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

將報告計量資料之裝置的 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 介面指標。

</dd> <dt>

*pProgressCallback* \[在\]
</dt> <dd>

進度回呼，應用程式可以透過此回呼來追蹤事件的進度，或取消事件。 進度是由 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)方法的 *EventId* 參數所識別。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

下列其中一個或兩個旗標的邏輯 **or** ，指定要執行的動作。 此值會從 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)的 *pdwStatus* 參數中取出。 您可以直接使用 *pdwStatus* 旗標。



| 旗標                        | 描述                                   |
|-----------------------------|-----------------------------------------------|
| WMDRM \_ 裝置 \_ NEEDCLOCK    | 從安全的時鐘伺服器取得時鐘。   |
| WMDRM \_ 裝置 \_ REFRESHCLOCK | 從安全的時鐘伺服器更新時鐘。 |



 

</dd> <dt>

*pdwStatus* \[擴展\]
</dt> <dd>

下列其中一個 **DWORD** 值，指定裝置所傳回的狀態。



| 狀態 | 描述                                                     |
|--------|-----------------------------------------------------------------|
| 0      | 不支援此動作。                                    |
| 1      | 無法從服務取得裝置安全時鐘。 |
| 2      | 無法設定裝置的安全時鐘。                     |
| 3      | 裝置的安全時鐘已設定。                              |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                                             | Description                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                                    | 此方法已成功。<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | 一或多個引數無效。<br/>                                                                                     |
| <dl> <dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt> </dl>                        | 指定的裝置不是 Windows Media DRM 相容裝置。<br/>                                                       |
| <dl> <dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 取得 \_ 安全 \_ 時鐘**</dt> </dl>               | 無法從裝置取得安全的時鐘挑戰，或無法從挑戰中取得安全的時鐘 URL。<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ 無法 \_ \_ \_ \_ \_ 從伺服器取得安全時鐘 \_**</dt> </dl> | 無法從安全的時鐘伺服器取得安全的時鐘回應。<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ 無法 \_ \_ 設定 \_ 安全 \_ 時鐘**</dt> </dl>               | 無法將安全時鐘挑戰傳送到裝置，或裝置無法設定時鐘。<br/>                          |



 

## <a name="remarks"></a>備註

這是非同步方法;裝置必須等待此作業的 [**IWMDMProgress：： End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) 回呼，才能嘗試播放任何授權的內容。

應用程式可以藉由呼叫 [**IWMDRMDeviceApp：： QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) 或 [**IWMDRMDeviceApp2：： QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)，來瞭解裝置是否必須重設或更新時鐘。

您的應用程式必須具有網際網路連線，才能讓它取得或重設安全的時鐘。

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

[**IWMDMProgress3 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp 介面**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





