---
description: CreateQueryWriterFromReader 方法的 Proxy 函式。
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945078"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a>IWICImagingFactory \_ CreateQueryWriterFromReader \_ Proxy 函式

[**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFactory* \[在\]
</dt> <dd>

類型： **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_pIQueryReader * \[ in\]
</dt> <dd>

類型： **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

中繼資料查詢讀取器，用來建立中繼資料寫入器。

</dd> <dt>

_pguidVendor * \[ in\]
</dt> <dd>

類型： **CONST GUID \** _

中繼資料查詢寫入器的廠商 GUID。

</dd> <dt>

_ppIQueryWriter * \[ out\]
</dt> <dd>

類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

接收新 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)指標的指標。

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



 

 




