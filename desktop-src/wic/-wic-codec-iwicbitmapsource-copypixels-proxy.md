---
description: CopyPixels 方法的 Proxy 函式。
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194411"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>IWICBitmapSource \_ CopyPixels \_ Proxy 函式

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

這個 [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。

</dd> <dt>

*中國* \[在\]
</dt> <dd>

類型： **Const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

要複製的矩形。 Null 值會指定整個點陣圖。

</dd> <dt>

_cbStride * \[ in\]
</dt> <dd>

類型： **UINT**

點陣圖的 stride

</dd> <dt>

*cbBufferSize* \[在\]
</dt> <dd>

類型： **UINT**

緩衝區的大小。

</dd> <dt>

*pbBuffer* \[擴展\]
</dt> <dd>

類型： **BYTE \** _

緩衝區的指標。

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



 

 




