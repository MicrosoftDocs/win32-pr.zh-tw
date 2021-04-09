---
description: SetSize 方法會變更資料流程物件的大小。
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer：： SetSize 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945040"
---
# <a name="ibytebuffersetsize-method"></a>IByteBuffer：： SetSize 方法

\[**SetSize** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**SetSize** 方法會變更資料流程物件的大小。

## <a name="syntax"></a>語法


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*libNewSize* \[在\]
</dt> <dd>

資料流程的新大小，以位元組數表示

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

**IByteBuffer：： SetSize** 方法會變更資料流程物件的大小。 呼叫這個方法來預先配置資料流程的空間。 如果 *libNewSize* 參數大於目前的資料流程大小，則會以位元組的未定義值填滿中間的空間，將資料流程延伸至指定的大小。 如果 seek 指標超過目前的資料流程結尾，則這項作業類似于 [**IByteBuffer：： Write**](ibytebuffer-write.md) 方法。

如果 *libNewSize* 參數小於目前的資料流程，則資料流程會截斷為指定的大小。

搜尋指標不受資料流程大小變更的影響。

呼叫 **IByteBuffer：： SetSize** 可能是嘗試取得大型連續空間區塊的有效方式。

## <a name="examples"></a>範例

下列範例會示範如何設定緩衝區大小。


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardssp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

