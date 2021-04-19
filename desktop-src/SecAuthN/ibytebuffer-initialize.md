---
description: Initialize 方法會準備要使用的 IByteBuffer 物件。 在呼叫 IByteBuffer 介面中的任何其他方法之前，必須先呼叫這個方法。
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'IByteBuffer：： Initialize 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990410"
---
# <a name="ibytebufferinitialize-method"></a>IByteBuffer：： Initialize 方法

\[**Initialize** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Initialize** 方法會準備要使用的 [**IByteBuffer**](ibytebuffer.md)物件。 在呼叫 **IByteBuffer** 介面中的任何其他方法之前，必須先呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lSize* \[在\]
</dt> <dd>

資料流程所要包含之資料的初始大小（以位元組為單位）。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

如果不是 **Null**，則為要寫入資料流程的初始資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

使用新的 [**IByteBuffer**](ibytebuffer.md) 資料流程時，請在使用任何其他 **IByteBuffer** 方法之前呼叫這個方法。

## <a name="examples"></a>範例

下列範例示範如何初始化 [**IByteBuffer**](ibytebuffer.md) 物件。


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
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



 

