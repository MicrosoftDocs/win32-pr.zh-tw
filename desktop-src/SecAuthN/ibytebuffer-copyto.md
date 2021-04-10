---
description: CopyTo 方法會將指定的位元組數目從物件中目前的搜尋指標複製到另一個物件中目前的搜尋指標。
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'IByteBuffer：： CopyTo 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194523"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer：： CopyTo 方法

\[**CopyTo** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**CopyTo** 方法會將指定的位元組數目從物件中目前的搜尋指標複製到另一個物件中目前的搜尋指標。

## <a name="syntax"></a>語法


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pByteBuffer* \[在\]
</dt> <dd>

指向目的地資料流程。 *PByteBuffer* 所指向的資料流程可以是新的資料流程或來來源資料流的複製。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

要從來來源資料流複製的位元組數目。

</dd> <dt>

*pcbRead* \[擴展\]
</dt> <dd>

位置的指標，此方法會寫入從來源讀取的實際位元組數目。 您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。 在此情況下，這個方法不會提供實際讀取的位元組數目。

</dd> <dt>

*pcbWritten* \[擴展\]
</dt> <dd>

位置的指標，此方法會寫入寫入目的地的實際位元組數目。 您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。 在此情況下，這個方法不會提供實際寫入的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

這個方法會將指定的位元組從某個資料流程複製到另一個資料流程。 它也可以用來將資料流程複製到本身。 每個資料流程實例中的 seek 指標都會針對讀取或寫入的位元組數進行調整。

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



 

