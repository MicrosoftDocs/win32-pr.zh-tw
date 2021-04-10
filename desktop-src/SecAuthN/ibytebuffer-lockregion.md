---
description: 限制存取緩衝區物件中指定的位元組範圍。
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer：： LockRegion 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194520"
---
# <a name="ibytebufferlockregion-method"></a>IByteBuffer：： LockRegion 方法

\[**LockRegion** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**LockRegion** 方法會限制存取緩衝區物件中指定的位元組範圍。

## <a name="syntax"></a>語法


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*libOffset* \[在\]
</dt> <dd>

整數，指定範圍開頭的位元組位移。

</dd> <dt>

*cb* \[在\]
</dt> <dd>

整數，指定要限制的範圍長度（以位元組為單位）。

</dd> <dt>

*dwLockType* \[在\]
</dt> <dd>

指定存取範圍時所要求的限制。 這可以是下表中的其中一個值。



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**鎖定 \_ 寫入**</dt> </dl>             | 您可以開啟指定的位元組範圍並讀取任意次數，但除非授與此鎖定的擁有者，否則不允許寫入鎖定範圍。<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**\_獨佔鎖定**</dt> </dl> | 除了授與此鎖定的擁有者之外，禁止寫入至指定的位元組範圍。<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**鎖定 \_ ONLYONCE**</dt> </dl>    | 如果授與此鎖定，就不能 \_ 取得範圍的其他鎖定 ONLYONCE 鎖定。 此鎖定類型通常是某些其他鎖定類型的別名。 因此，特定的執行可以有與此鎖定類型相關聯的其他行為。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

位元組範圍可延伸超過資料流程的目前結尾。 鎖定超過資料流程的結尾，會因為資料流程的不同實例之間的通訊方法而有所説明，而不會變更實際上是資料流程一部分的資料。

可支援三種類型的鎖定：鎖定以排除其他寫入器、鎖定排除其他讀取器或寫入器，以及只允許一個要求者取得指定範圍的鎖定，這通常是其他兩種鎖定類型之一的別名。 給定的資料流程實例可能會支援前兩種類型的其中一種，或兩者都支援。 鎖定類型是由 *dwLockType* 所指定，並使用 [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) 列舉中的值。

使用 **LockRegion** 鎖定的任何區域，稍後都必須使用與 *libOffset*、 *cb* 和 *dwLockType* 參數完全相同的值來呼叫 [**IByteBuffer：： UnlockRegion**](ibytebuffer-unlockregion.md) ，以明確解除鎖定。 區域必須在串流發行之前解除鎖定。 兩個連續的區域不能個別鎖定，然後使用單一解除鎖定呼叫來解除鎖定。

## <a name="examples"></a>範例

下列範例顯示限制對位元組範圍的存取。


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
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



 

