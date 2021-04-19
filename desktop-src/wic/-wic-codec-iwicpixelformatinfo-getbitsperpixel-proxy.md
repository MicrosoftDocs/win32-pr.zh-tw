---
description: GetBitsPerPixel 方法的 Proxy 函式。
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997908"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a>IWICPixelFormatInfo \_ GetBitsPerPixel \_ Proxy 函式

[**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

這個 [_ *IWICPixelFormatInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)物件的指標。

</dd> <dt>

*puiBitsPerPixel* \[擴展\]
</dt> <dd>

類型： **UINT \** _

接收像素格式 BPP 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




