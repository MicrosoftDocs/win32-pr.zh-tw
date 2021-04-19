---
title: 'ActiveBasicDevice SetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
description: '取得裝置的快取接收通訊協定資訊。 |ActiveBasicDevice SetCachedSinkProtocolInfo 方法 (PlayToDevice .h) '
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- SetCachedSinkProtocolInfo 方法媒體串流 API
- SetCachedSinkProtocolInfo 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，SetCachedSinkProtocolInfo 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988567"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>ActiveBasicDevice：： SetCachedSinkProtocolInfo 方法

取得裝置的快取接收通訊協定資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*physicalNetworkInterface* \[在\]
</dt> <dd>

指定實體網路介面。

</dd> <dt>

*位元速率* \[在\]
</dt> <dd>

位元速率值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

