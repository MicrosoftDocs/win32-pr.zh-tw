---
description: GetEnumerator 方法的 Proxy 函式。
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992085"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a>IWICMetadataQueryReader \_ GetEnumerator \_ Proxy 函式

[**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

這個 [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)物件的指標。

</dd> <dt>

*ppIEnumString* \[擴展\]
</dt> <dd>

類型： **IEnumString \* \***

接收中繼資料列舉值指標的指標。

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



 

 




