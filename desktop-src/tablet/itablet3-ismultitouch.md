---
description: 判斷輸入裝置是否支援多點觸控。
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: ITablet3：： IsMultiTouch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: bbdd18d27c8b9f5f4b7567e6aa22fd0c74f5e2c2dc74d80e1f46aca4195b93ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717297"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3：： IsMultiTouch 方法

判斷輸入裝置是否支援多點觸控。

## <a name="syntax"></a>語法


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIsMultiTouch* \[擴展\]
</dt> <dd>

指出裝置是否為多點觸控。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功 **時 \_ 傳回** ，否則 **\_ 會** 傳回錯誤碼，例如 E。

## <a name="remarks"></a>備註

在透過 [**IRealTimeStylus3：： MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) 或 **ITablet3：： IsMultiTouch** 判斷是否有多點觸控功能之後，應用程式可能會加入宣告多點觸控輸入訊息。 您可以在 **IRealTimeStylus3：： MultiTouchEnabled** 屬性區段中找到篩選多點觸控方法的其他資訊。

## <a name="examples"></a>範例


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




