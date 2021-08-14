---
description: CDeferredCommand。 CDeferredCommand 函式-函數方法。
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: 'CDeferredCommand. CDeferredCommand (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c45979437c153e70aea16c6b6e48b052b0d84491dcd1880075c66c77c777d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822223"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>CDeferredCommand. CDeferredCommand 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pq* 
</dt> <dd>

公開 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) 介面之物件的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

用於匯總的外部 **IUnknown** 介面指標。

</dd> <dt>

*phr* 
</dt> <dd>

傳回之 **HRESULT** 值的指標。

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

將執行此命令之物件的指標。

</dd> <dt>

*time* 
</dt> <dd>

執行命令的時間。

</dd> <dt>

*Iid* 
</dt> <dd>

包含方法之介面 (**GUID**) 的全域唯一識別碼指標。

</dd> <dt>

*dispidMethod* 
</dt> <dd>

要呼叫的介面上的方法。

</dd> <dt>

*wFlags* 
</dt> <dd>

調用的內容。

</dd> <dt>

*cArgs* 
</dt> <dd>

傳遞的引數數目。

</dd> <dt>

*pDispParams* 
</dt> <dd>

引數變異類型清單的指標。

</dd> <dt>

*pvarResult* 
</dt> <dd>

傳回之 variant 型別清單的指標（如果有的話）。

</dd> <dt>

*>puargerr* 
</dt> <dd>

包含錯誤之 *pDispParams* 參數清單中最後一個引數的指標。

</dd> <dt>

*bStream* 
</dt> <dd>

指出延後命令時間是否為數據流時間 (**TRUE**) 或呈現時間 (**FALSE**) 的值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




