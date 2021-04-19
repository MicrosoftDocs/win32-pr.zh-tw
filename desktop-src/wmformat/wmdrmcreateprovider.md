---
title: 'WMDRMCreateProvider 函式 (Wmdrmsdk) '
description: WMDRMCreateProvider 函式會建立可建立其他 Windows Media DRM 用戶端擴充 Api 物件的 class factory。
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- WMDRMCreateProvider 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992825"
---
# <a name="wmdrmcreateprovider-function"></a>WMDRMCreateProvider 函式

**WMDRMCreateProvider** 函式會建立可建立其他 WINDOWS Media DRM 用戶端擴充 api 物件的 class factory。 此函式不需要來自 Microsoft 的存根程式庫，並會建立不支援受保護 DRM 功能的物件。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**函式**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





