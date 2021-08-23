---
description: InitializeFromBitmap 方法的 Proxy 函式。
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c807e95b980a564096216727315f4a1534e8cd011cc78aa7322f670fff0876c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088180"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a>IWICPalette \_ InitializeFromBitmap \_ Proxy 函式

[**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

這個 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) 物件的指標。

</dd> <dt>

*pISurface* \[在\]
</dt> <dd>

類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

來源點陣圖的指標。

</dd> <dt>

*colorCount* \[在\]
</dt> <dd>

類型： **UINT**

用來初始化調色板的色彩數目。

</dd> <dt>

*fAddTransparentColor* \[在\]
</dt> <dd>

類型： **BOOL**

值，指出是否要加入透明色彩。

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



 

 




