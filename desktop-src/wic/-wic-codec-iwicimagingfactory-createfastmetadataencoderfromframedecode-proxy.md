---
description: CreateFastMetadataEncoderFromFrameDecode 方法的 Proxy 函式。
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996949"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a>IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode \_ Proxy 函式

[**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFactory* \[在\]
</dt> <dd>

類型： **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_pIFrameDecoder * \[ in\]
</dt> <dd>

類型： **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

用來建立 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)的 [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。

</dd> <dt>

*ppIFME* \[擴展\]
</dt> <dd>

類型： **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***

接收新 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)指標的指標。

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



 

 




