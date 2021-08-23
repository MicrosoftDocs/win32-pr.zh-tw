---
title: 'WMDRMShutdown 函式 (Wmdrmsdk) '
description: WMDRMShutdown 函式會釋放 Windows 媒體 DRM 用戶端擴充 api 所使用的資源。
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- WMDRMShutdown 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80f0f7264cd0962cb642f0877ccd044e777c3e9f269f87fcffc0037dcc0836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930362"
---
# <a name="wmdrmshutdown-function"></a>WMDRMShutdown 函式

**WMDRMShutdown** 函式會釋放 Windows 媒體 DRM 用戶端擴充 api 所使用的資源。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

若要避免記憶體流失，您必須針對 [**WMDRMStartup**](wmdrmstartup.md) 函式的每個呼叫呼叫此函數。

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

 

 





