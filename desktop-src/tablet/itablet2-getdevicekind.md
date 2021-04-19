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
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995846"
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

這個介面和方法是在 Windows Vista 中引進的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
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

 

 




