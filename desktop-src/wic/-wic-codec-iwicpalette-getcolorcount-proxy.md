---
description: GetColorCount 方法的 Proxy 函式。
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 18d06760c696bb3e95dc638bea31d02228a108b9866e213013243ad4eeec441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206327"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a>IWICPalette \_ GetColorCount \_ Proxy 函式

[**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

這個 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) 物件的指標。

</dd> <dt>

*pcCount* \[擴展\]
</dt> <dd>

類型： **UINT \***

接收色彩表中色彩數目的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP SP2，僅 Windows Vista \[ 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




