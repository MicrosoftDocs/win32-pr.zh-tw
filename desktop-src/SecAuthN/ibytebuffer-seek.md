---
description: Seek 方法會將搜尋指標變更為相對於緩衝區開頭、緩衝區結尾或目前搜尋指標的新位置。
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer：： Seek 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70c4af327fad5014c5d6dec80dd29441f51a03639a108249991c83f53e5d2be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016248"
---
# <a name="ibytebufferseek-method"></a>IByteBuffer：： Seek 方法

\[**Seek** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Seek** 方法會將搜尋指標變更為相對於緩衝區開頭、緩衝區結尾或目前搜尋指標的新位置。

## <a name="syntax"></a>語法


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dlibMove* \[在\]
</dt> <dd>

要加入至 *>dworigin* 所指示之位置的位移。 如果 *>dworigin* 是資料流程 \_ 搜尋 \_ 集，這會被視為不帶正負號的值而非正負號。

</dd> <dt>

*>dworigin* \[在\]
</dt> <dd>

指定 *dlibMove* 中指定之位移的原點。 來源可以是下表中的其中一個值。



| 值                                                                                                                                                                | 意義                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**串流 \_ 搜尋 \_ 集合**</dt> </dl> | 新的 seek 指標是相對於資料流程開頭的位移。 在此情況下， *dlibMove* 參數是相對於資料流程開頭的新搜尋位置。<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**串流 \_ 搜尋的 \_ 當前**</dt> </dl> | 新的 seek 指標是相對於目前搜尋指標位置的位移。 在此情況下， *dlibMove* 參數是來自目前搜尋位置的帶正負號的位移。<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**資料流程 \_ 搜尋 \_ 結束**</dt> </dl> | 新的 seek 指標是相對於資料流程結尾的位移。 在此情況下， *dlibMove* 參數是相對於資料流程結尾的新搜尋位置。<br/>             |



 

</dd> <dt>

*plibNewPosition* \[擴展\]
</dt> <dd>

位置的指標，這個方法會從資料流程的開頭處寫入新 seek 指標的值。 您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。 在此情況下，這個方法不會提供新的 seek 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

**Seek** 方法會變更 Seek 指標，讓後續的讀取和寫入作業可以在資料流程物件中的不同位置進行。 在資料流程的開頭之前搜尋是一項錯誤。 但是，它並不是搜尋超過資料流程結尾的錯誤。 搜尋超過資料流程的結尾適用于後續的寫入作業，因為資料流程將會在寫入作業完成之前，立即延伸至搜尋位置。

您也可以使用這個方法來取得 seek 指標的目前值，方法是呼叫這個方法，並將 *>dworigin* 參數設定為 [串流 \_ 搜尋] \_ ，並將 *dlibMove* 參數設為零，讓 seek 指標不會變更。 目前的 seek 指標會在 *plibNewPosition* 參數中傳回。

## <a name="examples"></a>範例

下列範例顯示如何將搜尋指標定位至新位置。


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardssp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

