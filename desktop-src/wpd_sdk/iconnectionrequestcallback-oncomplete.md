---
description: 通知應用程式先前排定的連線或對 MTP/藍牙裝置的中斷連線要求已完成。
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'IConnectionRequestCallback：： OnComplete 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843186"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback：： OnComplete 方法

**OnComplete** 方法會通知應用程式先前排定的連線或中斷對 MTP/藍牙裝置的要求已完成

## <a name="syntax"></a>語法


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hrStatus* \[在\]
</dt> <dd>

連接或中斷指定裝置連線的要求狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

應用程式會執行 [**IConnectionRequestCallback**](iconnectionrequestcallback.md) 介面，以接收有關已完成要求的通知，以及解除擱置的要求。

Windows可攜式裝置 (WPD) 呼叫這個方法，以通知應用程式先前已排程的要求已完成。 每個要求都可以透過應用程式提供的回呼來追蹤和取消。 因此，如果應用程式需要使用相同的 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)物件同時傳送多個要求，則每個要求都應傳遞唯一的 [**IConnectionRequestCallback**](iconnectionrequestcallback.md)物件做為 [**IPortableDeviceConnector：：連線**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect)和 [**IPortableDeviceConnector：:D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)方法的輸入參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




