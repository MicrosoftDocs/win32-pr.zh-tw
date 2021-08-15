---
description: 瞭解 IAMFilterData：： CreateFilterData 方法，它會建立篩選的二進位登錄資料。 這個介面已被取代。
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData：： CreateFilterData 方法 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 81c2ba3a56ba9c09a2ce7b23bcad1a83880e61256402c291b5aebde9988218c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428668"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IAMFilterData：： CreateFilterData 方法

> [!Note]  
> 這個介面已被取代。 新的應用程式不應使用它。

 

`CreateFilterData`方法會建立篩選的二進位登錄資料。 您可以 \_ 在篩選器的 CLSID 機碼底下，將此資料寫入登錄中作為名為 FilterData 的 REG 二進位子機碼。

應用程式通常不會呼叫這個方法。 [**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter)方法會自動建立二進位資料，並將它新增至登錄中的正確位置。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

## <a name="syntax"></a>語法


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prf2* \[在\]
</dt> <dd>

包含篩選資訊之 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 結構的指標。

</dd> <dt>

*prgbFilterData* \[擴展\]
</dt> <dd>

接收二進位資料指標之變數的位址。 方法會配置資料的記憶體。 呼叫端必須藉由呼叫 **CoTaskMemFree** 方法來釋放記憶體。

</dd> <dt>

*pcb* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收二進位資料的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果方法失敗，則會傳回錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭 Fil \_ data .h 位於 Windows SDK 的對應工具[範例](mapper-sample.md)目錄中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Fil \_ 資料。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMFilterData 介面**](iamfilterdata.md)
</dt> </dl>

 

 




