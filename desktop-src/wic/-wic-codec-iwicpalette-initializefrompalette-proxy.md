---
description: InitializeFromPalette 方法的 Proxy 函式。
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c5ba0efede61646a22f69b0809fabdd18f3ff1e2af3a02586caa61de38a5fc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668178"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a>IWICPalette \_ InitializeFromPalette \_ Proxy 函式

[**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

這個 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) 物件的指標。

</dd> <dt>

*pIMILPalette* \[在\]
</dt> <dd>

類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

來源調色板的指標。

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



 

 




