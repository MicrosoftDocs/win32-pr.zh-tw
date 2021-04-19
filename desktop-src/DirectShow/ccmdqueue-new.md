---
description: 新方法會初始化要執行的命令，並傳回新的 CDeferredCommand 物件。
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: 'CCmdQueue： New 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992782"
---
# <a name="ccmdqueuenew-method"></a>CCmdQueue 新方法

`New`方法會初始化要執行的命令，並傳回新的 [**CDeferredCommand**](cdeferredcommand.md)物件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCmd* 
</dt> <dd>

[**CDeferredCommand**](cdeferredcommand.md)物件的指標位址，應用程式可以透過此物件取消命令、為其設定新的呈現時間，或取得估計資訊。

</dd> <dt>

*朋 克* 
</dt> <dd>

將執行命令之物件的指標。

</dd> <dt>

*time* 
</dt> <dd>

執行佇列命令或命令的時間。

</dd> <dt>

*Iid* 
</dt> <dd>

要呼叫之介面 (**GUID**) 的全域唯一識別碼指標。

</dd> <dt>

*dispidMethod* 
</dt> <dd>

要呼叫的介面上的方法。

</dd> <dt>

*wFlags* 
</dt> <dd>

描述呼叫之內容的旗標。 此參數支援與 **IDispatch：： Invoke** 方法相同的旗標。

</dd> <dt>

*cArgs* 
</dt> <dd>

傳遞的引數數目。

</dd> <dt>

*pDispParams* 
</dt> <dd>

與分派參數相關聯之 variant 類型清單的指標。

</dd> <dt>

*pvarResult* 
</dt> <dd>

要傳回結果的清單（如果有的話）的指標。

</dd> <dt>

*>puargerr* 
</dt> <dd>

最後發生錯誤之 *pDispParams* 參數清單中索引的指標。

</dd> <dt>

*bStream* 
</dt> <dd>

值，指出 *time* 參數是否為數據流時間值 (**TRUE**) 或表示時間值 (**FALSE**) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 \_如果 *ppCmd* 從建立新的 [**CDeferredCommand**](cdeferredcommand.md)物件，其值為 **Null**，則傳回 E OUTOFMEMORY。 否則，會傳回 **HRESULT** ，表示嘗試建立新的 **CDeferredCommand** 物件時發生錯誤。 如果發生錯誤，則不會將任何物件排入佇列。

## <a name="remarks"></a>備註

新的 [**CDeferredCommand**](cdeferredcommand.md) 物件將會以參數進行初始化，並在結構化期間新增至佇列。 這個方法類似于 **IDispatch：： Invoke** 方法。

*WFlags* 參數的值包括下列各項：



| 值                    | 描述                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 分派 \_ 方法         | 成員正在以方法的形式執行。 如果屬性具有相同的名稱，則可以設定此和分派 \_ PROPERTYGET 旗標。                                       |
| 分派 \_ PROPERTYGET    | 正在將成員取出為屬性或資料成員。                                                                                                          |
| 分派 \_ PROPERTYPUT    | 成員正變更為屬性或資料成員。                                                                                                            |
| 分派 \_ PROPERTYPUTREF | 成員正在透過參考指派進行變更，而不是值指派。 只有當屬性接受物件的參考時，此值才有效。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




