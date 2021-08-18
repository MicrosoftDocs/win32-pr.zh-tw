---
description: Read 方法會從緩衝區物件中，將指定的位元組數目從目前的 seek 指標開始讀取到記憶體中。
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer：： Read 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482668"
---
# <a name="ibytebufferread-method"></a>IByteBuffer：： Read 方法

\[**Read** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Read** 方法會從緩衝區物件中，將指定的位元組數目從目前的 seek 指標開始讀取到記憶體中。

## <a name="syntax"></a>語法


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pByte* \[擴展\]
</dt> <dd>

指向讀取資料流程資料的緩衝區。 如果發生錯誤，此值為 **Null**。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

嘗試從資料流程物件讀取的資料位元組數目。

</dd> <dt>

*pcbRead* \[擴展\]
</dt> <dd>

**長** 變數的位址，此變數會接收從資料流程物件讀取的實際位元組數目。 您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。 在此情況下，這個方法不會提供實際讀取的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

這個方法會將此資料流程物件的位元組讀入記憶體中。 資料流程物件必須以 STGM \_ 讀取模式開啟。 這個方法會以讀取的實際位元組數目來調整 seek 指標。

實際讀取的位元組數目也會在 *pcbRead* 參數中傳回。

給呼叫者的注意事項

如果發生錯誤，或是在讀取作業期間到達資料流程的結尾，則讀取的實際位元組數目可能會少於所要求的位元組數目。

如果在讀取期間到達資料流程的結尾，某些可能會傳回錯誤。 您必須準備好處理資料流程讀取結束時的錯誤傳回或 S \_ OK 傳回值。

## <a name="examples"></a>範例

下列範例會示範如何讀取緩衝區中的位元組。


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
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



 

