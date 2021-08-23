---
description: Set 方法會設定屬性集 GUID 和屬性識別碼所識別的屬性。
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet：： Set 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f3669acb7f2d3049b909a4dc2c24363bf478c9b44ad0a91528e1e8ea466399fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639188"
---
# <a name="ikspropertysetset-method"></a>IKsPropertySet：： Set 方法

`Set`方法會設定屬性集 GUID 和屬性識別碼所識別的屬性。

## <a name="syntax"></a>語法


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pInstanceData* \[在\]
</dt> <dd>

緩衝區的指標，此緩衝區包含屬性的實例資料。

</dd> <dt>

*cbInstanceData* \[在\]
</dt> <dd>

*PInstanceData* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pPropData* \[在\]
</dt> <dd>

包含屬性值之緩衝區的指標。

</dd> <dt>

*cbPropData* \[在\]
</dt> <dd>

*PPropData* 緩衝區的 Sise （以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                              | 描述                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 成功。<br/>                                                         |
| <dl> <dt>**E \_ \_ 設定 \_ 不支援的設定**</dt> </dl> | 不支援屬性集。<br/>                               |
| <dl> <dt>**E \_ \_ \_ 不支援的識別碼**</dt> </dl>  | 指定的屬性集不支援屬性識別碼。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 **IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。

 

您必須在 Ksproxy 之前包含 Ks。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ksproxy。h</dt> </dl>    |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet 介面**](ikspropertyset.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 




