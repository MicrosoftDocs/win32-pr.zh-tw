---
description: 初始化具有 IWICBitmapSource 的 IWICColorTransform，並將它從一個 IWICColorCoNtext 轉換成另一個。
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995279"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>IWICColorTransform \_ Initialize \_ Proxy 函式

初始化具有 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)的 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) ，並將它從一個 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)轉換成另一個。

## <a name="syntax"></a>語法


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIColorTransform* \[在\]
</dt> <dd>

類型： **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

要初始化的色彩轉換。

</dd> <dt>

*pIBitmapSource* \[在\]
</dt> <dd>

類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

用來初始化色彩轉換的點陣圖來源。

</dd> <dt>

*pICoNtextSource* \[在\]
</dt> <dd>

類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

色彩內容來源。

</dd> <dt>

*pICoNtextDest* \[在\]
</dt> <dd>

類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

色彩內容目的地。

</dd> <dt>

*pixelFmtDest* \[在\]
</dt> <dd>

類型： **REFWICPixelFormatGUID**

所需像素格式的 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




