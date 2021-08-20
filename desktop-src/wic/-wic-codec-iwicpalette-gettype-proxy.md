---
description: GetType 方法的 Proxy 函數。
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1c4b9c0d17b37be8ff2d5db85f112e528b0d9e447856e387c63a5f436d59376a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668169"
---
# <a name="iwicpalette_gettype_proxy-function"></a>IWICPalette \_ GetType \_ Proxy 函式

[**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype)方法的 Proxy 函數。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

這個 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) 物件的指標。

</dd> <dt>

*pePaletteType* \[擴展\]
</dt> <dd>

類型： **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\***

接收 bimtap 之調色板型別的指標。

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



 

 




