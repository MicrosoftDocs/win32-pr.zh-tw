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
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194414"
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
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




