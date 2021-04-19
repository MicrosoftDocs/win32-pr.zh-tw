---
description: GetMetadataByName 方法的 Proxy 函式。
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000159"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a>IWICMetadataQueryReader \_ GetMetadataByName \_ Proxy 函式

[**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

這個 [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)物件的指標。

</dd> <dt>

*wzName* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要求的中繼資料專案名稱。

</dd> <dt>

*pvarValue* \[in、out\]
</dt> <dd>

類型： **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

接收中繼資料屬性的指標。

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



 

