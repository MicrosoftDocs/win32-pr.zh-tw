---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975425"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a>IWICBitmapEncoder \_ Initialize \_ Proxy 函式

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _

這個 [_ *IWICBitmapEncoder* *](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。

</dd> <dt>

*pIStream* \[在\]
</dt> <dd>

類型： **[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _

輸出資料流。

</dd> <dt>

_cacheOption * \[ in\]
</dt> <dd>

類型： **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**

初始化時使用的 [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) 。

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



 

