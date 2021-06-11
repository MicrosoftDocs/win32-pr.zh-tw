---
description: 深入瞭解 IAMFilterData：:P arseFilterData 方法，解壓縮篩選的二進位登錄資料。 這個介面已被取代。
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData：:P arseFilterData 方法 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989443"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData：:P arseFilterData 方法

> [!Note]  
> 這個介面已被取代。 新的應用程式不應使用它。

 

`ParseFilterData`方法會解壓縮篩選的二進位登錄資料。

應用程式通常不會呼叫這個方法。 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)方法提供更方便的方式來存取篩選登錄資料。

## <a name="syntax"></a>語法


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rgbFilterData* \[在\]
</dt> <dd>

二進位登錄資料的指標。 您可以從篩選器的標記中抓取 "FilterData" 屬性來取得此資料。 資料會儲存為位元組的 **SAFEARRAY** (vt \_ UI1 \| vt \_ 陣列) 。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

指定二進位資料的大小（以位元組為單位）。

</dd> <dt>

*prgbRegFilter2* \[擴展\]
</dt> <dd>

接收已解壓縮資料指標之變數的位址。 當方法傳回時，將這個指標轉換成 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 類型以存取篩選資料。 呼叫端必須藉由呼叫 **CoTaskMemFree** 方法來釋放記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果方法失敗，則會傳回錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Fil \_ 資料。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMFilterData 介面**](iamfilterdata.md)
</dt> </dl>

 

 




