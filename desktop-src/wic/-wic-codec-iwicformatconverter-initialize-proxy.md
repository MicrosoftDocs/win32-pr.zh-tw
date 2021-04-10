---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194410"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>IWICFormatConverter \_ Initialize \_ Proxy 函式

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _

這個 [_ *IWICFormatConverter* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)物件的指標。

</dd> <dt>

*pISource* \[在\]
</dt> <dd>

類型： **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

要轉換的輸入點陣圖

</dd> <dt>

_dstFormat * \[ in\]
</dt> <dd>

類型： **REFWICPixelFormatGUID**

目的地像素格式 GUID。

</dd> <dt>

*遞色* \[在\]
</dt> <dd>

類型： **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

用於轉換的 [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) 。

</dd> <dt>

*pIPalette* \[在\]
</dt> <dd>

類型： **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

用於轉換的調色板。

</dd> <dt>

_AlphaThresholdPercent * \[ in\]
</dt> <dd>

類型： **double**

要用於轉換的 Alpha 臨界值。

</dd> <dt>

*paletteTranslate* \[在\]
</dt> <dd>

類型： **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

用於轉換的調色板轉譯類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




