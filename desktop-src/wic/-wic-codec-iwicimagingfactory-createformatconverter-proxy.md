---
description: CreateFormatConverter 方法的 Proxy 函式。
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194408"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a>IWICImagingFactory \_ CreateFormatConverter \_ Proxy 函式

[**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFactory* \[在\]
</dt> <dd>

類型： **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIFormatConverter * \[ out\]
</dt> <dd>

類型： **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***

接收新 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)指標的指標。

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



 

 




