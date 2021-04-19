---
description: 用於建立 IWICImagingFactory 的 Proxy 函數。
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986982"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>WICCreateImagingFactory \_ Proxy 函式

用於建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)的 Proxy 函數。

## <a name="syntax"></a>語法

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*SDKVersion* \[在\]
</dt> <dd>

類型： **UINT**

</dd> <dt>

*ppIImagingFactory* \[擴展\]
</dt> <dd>

類型： **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此函式是協助程式，可為 Windows XP 所需的明確 DLL 連結建立 WIC factory。 在正常使用方式下，您會改為使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (請參閱 [WIC API class](./-wic-api.md#class-factories) factory) ，因為這一律包含在所有較新版本的 Windows 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll;</dt><dt>windowscodecs .lib</dt> </dl> |



 

