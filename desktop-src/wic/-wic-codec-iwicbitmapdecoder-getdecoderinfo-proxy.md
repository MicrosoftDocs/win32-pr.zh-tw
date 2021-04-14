---
description: GetDecoderInfo 方法的 Proxy 函式。
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: IWICBitmapDecoder_GetDecoderInfo_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468972"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a>IWICBitmapDecoder \_ GetDecoderInfo \_ Proxy 函式

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

這個 [_ *IWICBitmapDecoder* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。

</dd> <dt>

*ppIDecoderInfo* \[擴展\]
</dt> <dd>

類型： **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***

接收 [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)指標的指標。

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



 

 




