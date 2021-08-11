---
title: 'ActiveBasicDevice GetCachedBitrateMeasurement 方法 (PlayToDevice .h) '
description: 取得快取的位元速率。
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- GetCachedBitrateMeasurement 方法媒體串流 API
- GetCachedBitrateMeasurement 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetCachedBitrateMeasurement 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236863"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>ActiveBasicDevice：： GetCachedBitrateMeasurement 方法

取得快取的位元速率。

## <a name="syntax"></a>語法


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*physicalNetworkInterface* \[在\]
</dt> <dd>

指定實體網路介面。

</dd> <dt>

*位元速率* \[退出，retval\]
</dt> <dd>

接收位元速率值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

