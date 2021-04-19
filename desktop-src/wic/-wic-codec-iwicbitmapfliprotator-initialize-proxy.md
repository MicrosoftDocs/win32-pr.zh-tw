---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970407"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a>IWICBitmapFlipRotator \_ Initialize \_ Proxy 函式

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _

這個 [_ *IWICBitmapFlipRotator* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)物件的指標。

</dd> <dt>

*pISource* \[在\]
</dt> <dd>

類型： **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

輸入點陣圖來源。

</dd> <dt>

_options * \[ in\]
</dt> <dd>

類型： **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**

要翻轉或旋轉影像的 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 。

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



 

 




