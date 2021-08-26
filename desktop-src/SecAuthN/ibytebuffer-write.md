---
description: Write 方法會將指定的數位從目前搜尋指標開始的資料流程物件寫入資料流程物件。
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer：： Write 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0033d4f4ee03629d2bedf9f232a43607100bcdca8bfaab457c2236bbfad603d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127348"
---
# <a name="ibytebufferwrite-method"></a>IByteBuffer：： Write 方法

\[**Write** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Write** 方法會將指定的數位從目前搜尋指標開始的資料流程物件寫入資料流程物件。

## <a name="syntax"></a>語法


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pByte* \[在\]
</dt> <dd>

包含要寫入至資料流程之資料的緩衝區位址。 即使 *cb* 為零，也必須為此參數提供有效的指標。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

嘗試寫入資料流程的資料位元組數。 這個參數可以是零。

</dd> <dt>

*pcbWritten* \[擴展\]
</dt> <dd>

**長** 變數的位址，這個方法會寫入寫入資料流程物件的實際位元組數目。 呼叫端可以將 this 指標設為 **Null**，在此情況下，這個方法不會提供實際寫入的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

**IByteBuffer：： Write** 方法會將指定的資料寫入資料流程物件。 搜尋指標會針對實際寫入的位元組數進行調整。 實際寫入的位元組數目會在 *pcbWritten* 參數中傳回。 如果位元組計數為零個位元組，則寫入作業不會有任何作用。

如果 seek 指標目前超過資料流程的結尾，而且位元組計數為非零值，則這個方法會將資料流程的大小增加到 seek 指標，並從 seek 指標開始寫入指定的位元組。 寫入資料流程的填滿位元組不會初始化為任何特定的值。 這與 MS-DOS FAT 檔案系統中的檔案結尾行為相同。

若使用零位元組計數和超出資料流程結尾的 seek 指標，此方法不會建立填滿位元組來將資料流程增加到 seek 指標。 在此情況下，您必須呼叫 [**IByteBuffer：： SetSize**](ibytebuffer-setsize.md) 方法，以增加資料流程的大小並寫入填滿位元組。

*PcbWritten* 參數可以有值（即使發生錯誤）。

在 COM 提供的執行中，資料流程物件並不是稀疏的。 任何填滿的位元組最後都會配置在磁片上，並指派給串流。

## <a name="examples"></a>範例

下列範例示範如何將位元組寫入資料流程物件。


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
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



 

