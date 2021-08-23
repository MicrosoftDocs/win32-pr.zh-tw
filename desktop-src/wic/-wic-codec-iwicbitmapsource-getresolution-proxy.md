---
description: GetResolution 方法的 Proxy 函式。
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f226e1fddc1d780e24796d342736082c2f7f11e7d03369245f2222eee1074713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088350"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a>IWICBitmapSource \_ GetResolution \_ Proxy 函式

[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

這個 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件的指標。

</dd> <dt>

*pDpiX* \[擴展\]
</dt> <dd>

類型： **double \***

接收 X 軸 DPI 解析度的指標。

</dd> <dt>

*pDpiY* \[擴展\]
</dt> <dd>

類型： **double \***

接收 y 軸 DPI 解析度的指標。

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



 

 




