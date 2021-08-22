---
title: 'ActiveBasicDevice GetCachedExtraSinkProtocolInfo 方法 (PlayToDevice .h) '
description: 取得裝置的其他快取接收通訊協定資訊。
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- GetCachedExtraSinkProtocolInfo 方法媒體串流 API
- GetCachedExtraSinkProtocolInfo 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetCachedExtraSinkProtocolInfo 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf4508c40fd0abcb0df809216a9bae1d8811c8a8bd79bfb31dfbbd5062ddce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736404"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>ActiveBasicDevice：： GetCachedExtraSinkProtocolInfo 方法

取得裝置的其他快取接收通訊協定資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

裝置的額外快取接收通訊協定資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

