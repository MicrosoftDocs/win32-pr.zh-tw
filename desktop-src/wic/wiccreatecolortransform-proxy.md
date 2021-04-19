---
description: 建立可執行 IWICColorTransform 的色彩轉換物件。 這個 COM 物件支援無限制執行緒的物件模型。
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995644"
---
# <a name="wiccreatecolortransform_proxy-function"></a>WICCreateColorTransform \_ Proxy 函式

建立可執行 [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform)的色彩轉換物件。 這個 COM 物件支援無限制執行緒的物件模型。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIColorTransform* \[擴展\]
</dt> <dd>

建立的色彩轉換。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
