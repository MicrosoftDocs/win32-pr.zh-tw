---
description: Commit 方法可確保在交易模式中開啟之物件所做的任何變更，都會反映在父儲存體中。
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer：： Commit 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: af165e6f0a805532eade820dcb67968a77186cee3f90cfc48a240d387b1f31b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127408"
---
# <a name="ibytebuffercommit-method"></a>IByteBuffer：： Commit 方法

\[**Commit** 方法可在 [需求] 區段中指定的作業系統中使用。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**Commit** 方法可確保在交易模式中開啟之物件所做的任何變更，都會反映在父儲存體中。

## <a name="syntax"></a>語法


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*grfCommitFlags* \[在\]
</dt> <dd>

控制資料流物件的變更如何認可。 如需這些值的定義，請參閱 STGC 列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 S \_ OK 表示呼叫成功。

## <a name="remarks"></a>備註

這個方法可確保在交易模式中開啟之資料流程物件的變更會反映在父儲存體中。 自從開啟或上次認可之後對資料流程所做的變更，都會反映在父儲存物件中。 如果以交易模式開啟父系，父系可能仍會在稍後回復此資料流程物件的變更時還原。 複合檔案的執行不支援在交易模式中開啟資料流程，因此這個方法的效果幾乎不會影響到清除記憶體緩衝區。

## <a name="examples"></a>範例

下列範例顯示如何將變更認可至儲存體。


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
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



 

