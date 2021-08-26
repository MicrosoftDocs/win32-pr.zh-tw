---
description: SetResolution 方法的 IWICBitmap_SetResolution_Proxy 函數 Proxy 函式。
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a32fa4e0d830d5307bc2927a1d5b6cb0a40e5b21f86517dc4421a0ce246a2ab8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056698"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a>IWICBitmap \_ SetResolution \_ Proxy 函式

[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)方法的 Proxy 函式。

## <a name="syntax"></a>語法


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*這 \_* \[ 中的 PTR\]
</dt> <dd>

類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

這個 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) 物件的指標。

</dd> <dt>

*DPIX* \[在\]
</dt> <dd>

類型： **double**

水準解析度。

</dd> <dt>

*DPIY* \[在\]
</dt> <dd>

類型： **double**

垂直解析度。

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



 

 




