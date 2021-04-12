---
description: QuerySupported 方法會判斷物件是否支援指定的屬性集。
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'IKsPropertySet：： QuerySupported 方法 (Ks. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187472"
---
# <a name="ikspropertysetquerysupported-method"></a>IKsPropertySet：： QuerySupported 方法

`QuerySupported`方法會判斷物件是否支援指定的屬性集。

## <a name="syntax"></a>語法


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*guidPropSet* \[在\]
</dt> <dd>

屬性集 GUID。

</dd> <dt>

*dwPropID* \[在\]
</dt> <dd>

屬性集內屬性的識別碼。

</dd> <dt>

*pTypeSupport* \[擴展\]
</dt> <dd>

用來儲存旗標的值指標，指出驅動程式所提供的支援。 支援的旗標包含下列各項。



| 值                    | 描述                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| KSPROPERTY \_ 支援 \_ 取得 | 您可以藉由呼叫 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 方法來取得屬性。 |
| KSPROPERTY \_ 支援 \_ 集 | 您可以藉由呼叫 [**IKsPropertySet：： Set**](ikspropertyset-set.md)來變更屬性。              |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                              | Description                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 支援指定的屬性集和屬性 ID 組合。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                | 不支援屬性集。<br/>                                       |
| <dl> <dt>**E \_ \_ \_ 不支援的識別碼**</dt> </dl>  | 指定的屬性集不支援屬性識別碼。<br/>         |
| <dl> <dt>**E \_ \_ 設定 \_ 不支援的設定**</dt> </dl> | 不支援屬性集。<br/>                                       |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 **IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。

 

您必須在 Ksproxy 之前包含 Ks。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                             |
| 標頭<br/>                   | <dl> <dt>Ks. h;</dt><dt>Ksproxy .h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet 介面**](ikspropertyset.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 




