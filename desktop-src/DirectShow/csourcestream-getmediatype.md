---
description: GetMediaType 方法會捕獲慣用的媒體類型。 這個方法會使用 *ipositionsummaryview* 和 *pMediaType* 參數。
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: CSourceStream. GetMediaType 方法 (Source .h) -Ipositionsummaryview 和 pMediaType 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073252"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>CSourceStream. GetMediaType 方法 (Source .h) -Ipositionsummaryview 和 pMediaType 參數

**GetMediaType** 方法會捕獲慣用的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Ipositionsummaryview* 
</dt> <dd>

以零為基底的索引值。

</dd> <dt>

*pMediaType* 
</dt> <dd>

接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                            | 描述                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>              |
| <dl> <dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt> </dl> | 索引超出範圍。<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | 索引小於零。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>           | 非預期的錯誤。<br/>     |



 

## <a name="remarks"></a>備註

此方法有兩個版本。 其中一個版本會覆寫 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法，並接受索引值做為參數。 另一個版本是設計來取得單一媒體類型，因此它缺少索引參數。

單一參數方法會傳回 E 未 \_ 預期的。 雙參數方法會驗證 *ipositionsummaryview* 參數是否為零，然後呼叫單一參數版本。 根據 pin 所支援的媒體類型數目，您必須覆寫下列其中一種方法：

-   如果 pin 只支援一種媒體類型，請覆寫單一參數版本。 填入釘選支援的媒體類型。
-   如果 pin 支援一個以上的媒體類型，請覆寫兩個參數的版本。 也覆寫 [**CSourceStream：： CheckMediaType**](csourcestream-checkmediatype.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | 來源 .h (包含) 的資料流程                                                                                    |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




