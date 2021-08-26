---
description: 移除先前使用 IByteBuffer：： LockRegion 限制之位元組範圍的存取限制。
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'IByteBuffer：： UnlockRegion 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127388"
---
# <a name="ibytebufferunlockregion-method"></a>IByteBuffer：： UnlockRegion 方法

\[**UnlockRegion** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**UnlockRegion** 方法會移除先前使用 [**IByteBuffer：： LockRegion**](ibytebuffer-lockregion.md)限制之位元組範圍的存取限制。

## <a name="syntax"></a>語法


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*libOffset* \[在\]
</dt> <dd>

範圍開頭的位元組位移。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

要限制的範圍長度（以位元組為單位）。

</dd> <dt>

*dwLockType* \[在\]
</dt> <dd>

先前放置於範圍內的存取限制。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

**IByteBuffer：： UnlockRegion** 方法會解除鎖定先前使用 [**IByteBuffer：： LockRegion**](ibytebuffer-lockregion.md)方法鎖定的區域。 您稍後必須使用與 *libOffset*、 *cb* 和 *dwLockType* 參數完全相同的值來呼叫 **IByteBuffer：： UnlockRegion** ，以明確解除鎖定區域的鎖定。 區域必須在串流發行之前解除鎖定。 兩個連續的區域不能個別鎖定，然後使用單一解除鎖定呼叫來解除鎖定。

## <a name="examples"></a>範例

下列範例顯示解除鎖定某個範圍的位元組。


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
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



 

