---
description: 傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: ITablet2：： GetDeviceKind 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450525"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2：： GetDeviceKind 方法

傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pKind* \[擴展\]
</dt> <dd>

列舉值，指出平板電腦的類型，例如滑鼠、畫筆或觸控。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

Windows Vista 中引進了這個介面和方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet2 介面**](itablet2.md)
</dt> <dt>

[**平板電腦 \_ 裝置 \_ 種類列舉**](tablet-device-kind.md)
</dt> <dt>

[**ITablet 介面**](itablet.md)
</dt> </dl>

 

 




