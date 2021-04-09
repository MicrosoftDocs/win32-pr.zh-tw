---
description: 通知應用程式，已完成對 MTP/Bluetooth 裝置的先前排程連線或中斷連接要求。
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
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850407"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback：： OnComplete 方法

**OnComplete** 方法會通知應用程式先前已排程的連線，或對 MTP/Bluetooth 裝置的中斷連接要求已完成

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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

應用程式會執行 [**IConnectionRequestCallback**](iconnectionrequestcallback.md) 介面，以接收有關已完成要求的通知，以及解除擱置的要求。

Windows 可攜式裝置 (WPD) 呼叫這個方法，以通知應用程式先前已排程的要求已完成。 每個要求都可以透過應用程式提供的回呼來追蹤和取消。 因此，如果應用程式需要使用相同的 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 物件同時傳送多個要求，則每個要求都應傳遞唯一的 [**IConnectionRequestCallback**](iconnectionrequestcallback.md) 物件做為 [**IPortableDeviceConnector：： Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) 和 [**IPortableDeviceConnector：:D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) 方法的輸入參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




