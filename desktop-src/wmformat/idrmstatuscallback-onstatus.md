---
title: IDRMStatusCallback OnStatus 方法
description: OnStatus 方法會從非同步 DRM 進程接收狀態訊息。
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus 方法 windows Media 格式
- OnStatus 方法 windows Media Format，IDRMStatusCallback 介面
- IDRMStatusCallback 介面 windows Media Format，OnStatus 方法
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847452"
---
# <a name="idrmstatuscallbackonstatus-method"></a>IDRMStatusCallback：： OnStatus 方法

**OnStatus** 方法會從非同步 DRM 進程接收狀態訊息。

## <a name="syntax"></a>語法


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*狀態* \[在\]
</dt> <dd>

狀態碼。 訊息碼是在 **MSDRM \_ 狀態** 列舉類型中定義。

</dd> <dt>

*hr* \[在\]
</dt> <dd>

傳回支援狀態訊息的程式碼。

</dd> <dt>

*dwType* \[在\]
</dt> <dd>

*PValue* 所指向之資料的類型。 設定為 [**DRM \_ ATTR \_ DATATYPE**](drm-attr-datatype.md) 列舉值的其中一個值。

</dd> <dt>

*pValue* \[在\]
</dt> <dd>

與狀態訊息相關之資料的指標。 資料的類型取決於 *dwType* 參數的值。 如需詳細資訊，請參閱 [**DRM \_ ATTR \_ DATATYPE**](drm-attr-datatype.md) 列舉。

</dd> <dt>

*pvCoNtext* \[在\]
</dt> <dd>

選擇性參數，可用來識別傳送訊息的物件。 藉由在註冊此回呼時設定 *pvCoNtext* ，您可以使用相同的回呼來處理多個非同步處理常式。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ ATTR \_ 資料類型**](drm-attr-datatype.md)
</dt> <dt>

[**IDRMStatusCallback 介面**](idrmstatuscallback.md)
</dt> </dl>

 

 





