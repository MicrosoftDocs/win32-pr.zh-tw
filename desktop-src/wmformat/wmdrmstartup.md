---
title: 'WMDRMStartup 函式 (Wmdrmsdk) '
description: WMDRMStartup 函式會初始化 Windows Media DRM 用戶端擴充 Api 所使用的資源。
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- WMDRMStartup 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993212"
---
# <a name="wmdrmstartup-function"></a>WMDRMStartup 函式

**WMDRMStartup** 函式會初始化 WINDOWS Media DRM 用戶端擴充 api 所使用的資源。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

針對此函式的每個呼叫，您都必須呼叫 [**WMDRMShutdown**](wmdrmshutdown.md) 來釋放使用的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**函式**](drm-functions.md)
</dt> </dl>

 

 





