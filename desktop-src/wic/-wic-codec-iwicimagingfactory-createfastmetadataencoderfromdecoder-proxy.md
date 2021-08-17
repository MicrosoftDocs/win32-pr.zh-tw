---
description: CreateFastMetadataEncoderFromDecoder 方法的 Proxy 函式。
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8c08e5b60c33e2735272236be87bdf9250f6109f3434c833b353252feac976a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206393"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a>IWICImagingFactory \_ CreateFastMetadataEncoderFromDecoder \_ Proxy 函式

[**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFactory* \[在\]
</dt> <dd>

類型： **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*pIDecoder* \[在\]
</dt> <dd>

類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

用來建立 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) 的解碼器。

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
| 最低支援的用戶端<br/> | WindowsXP SP2，僅 Windows Vista \[ 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




