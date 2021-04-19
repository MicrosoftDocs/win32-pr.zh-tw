---
description: SetResolution 方法的 Proxy 函式。
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
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991818"
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

類型： **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _

這個 [_ *IWICBitmap* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)物件的指標。

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
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt> </dl> |



 

 




