---
title: 'WMDRMCreateProtectedProvider 函式 (Wmdrmsdk) '
description: WMDRMCreateProtectedProvider 函式會建立可建立 Windows 媒體 DRM 用戶端擴充 api 之其他物件的 class factory。
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- WMDRMCreateProtectedProvider 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026926"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>WMDRMCreateProtectedProvider 函式

**WMDRMCreateProtectedProvider** 函式會建立可建立 Windows 媒體 DRM 用戶端擴充 api 之其他物件的 class factory。 此函式需要來自 Microsoft 的存根程式庫，並建立支援受保護 DRM 功能的物件。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDRMProvider* \[擴展\]
</dt> <dd>

接收新建立物件之 [**IWMDRMProvider**](iwmdrmprovider.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**函式**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





