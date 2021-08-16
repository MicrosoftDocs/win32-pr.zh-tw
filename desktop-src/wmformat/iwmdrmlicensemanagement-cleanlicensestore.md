---
title: 'IWMDRMLicenseManagement CleanLicenseStore 方法 (Wmdrmsdk .h) '
description: CleanLicenseStore 方法會從暫時授權存放區中移除無法使用的授權，並重組本機授權存放區以改善效能。
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- CleanLicenseStore 方法 windows Media 格式
- CleanLicenseStore 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CleanLicenseStore 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846948"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>IWMDRMLicenseManagement：： CleanLicenseStore 方法

**CleanLicenseStore** 方法會從暫時授權存放區中移除無法使用的授權，並重組本機授權存放區以改善效能。

## <a name="syntax"></a>語法


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

旗標，指定要使用的授權存放清除選項。 設定為下表中的其中一個常數。



| 常數                            | 描述                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ 同步處理  | 清除作業將會同步執行。 在作業完成之前，不會傳回這個方法。                                                              |
| WMDRM \_ 乾淨 \_ 授權 \_ 商店 \_ ASYNC | 清除作業將會以非同步方式執行。 這個方法會立即傳回。 當作業完成時，將會傳送媒體事件 MELicenseStoreCleaned。 |



 

</dd> <dt>

*ppunkCancelationCookie* \[擴展\]
</dt> <dd>

指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。 這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                            | 描述                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 此方法已成功。<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | 用戶端電腦上沒有暫時性的授權存放區。<br/> |



 

## <a name="remarks"></a>備註

這個方法會以非同步方式執行。 它會在呼叫後立即傳回，然後在處理完成時產生 **MEWMDRMLicenseStoreCleaned** 事件。

如需使用 Windows 媒體 DRM 用戶端擴充 api 的非同步方法的詳細資訊，請參閱[使用媒體基礎事件模型](using-the-media-foundation-model.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





