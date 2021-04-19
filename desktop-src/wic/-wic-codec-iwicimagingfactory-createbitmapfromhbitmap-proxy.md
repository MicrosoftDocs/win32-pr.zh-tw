---
description: CreateBitmapFromHBITMAP 方法的 Proxy 函式。
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975248"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a>IWICImagingFactory \_ CreateBitmapFromHBITMAP \_ Proxy 函式

[**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFactory* \[在\]
</dt> <dd>

類型： **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hBitmap * \[ in\]
</dt> <dd>

類型： **HBITMAP**

用來建立點陣圖的點陣圖控制碼。

</dd> <dt>

*hPalette* \[在\]
</dt> <dd>

類型： **HPALETTE**

用來建立點陣圖的調色板控制碼。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**

用來建立點陣圖的 Alpha 通道選項。

</dd> <dt>

*ppIBitmap* \[擴展\]
</dt> <dd>

類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

接收新點陣圖指標的指標。

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



 

 




