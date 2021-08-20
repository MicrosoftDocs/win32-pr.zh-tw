---
description: 釋放由 RtlAllocateHeap 從堆積配置的記憶體區塊。
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: 'RtlFreeHeap 函式 (Ntifs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538070"
---
# <a name="rtlfreeheap-function"></a>RtlFreeHeap 函式

釋放由 [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)從堆積配置的記憶體區塊。

## <a name="syntax"></a>語法


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*HeapHandle* \[在\]
</dt> <dd>

要釋放其記憶體區塊之堆積的控制碼。 此參數是 [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)所傳回的控制碼。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

一組旗標，可控制釋放記憶體區塊的各個層面。 指定下列值，可覆寫 [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)建立堆積時，*旗標* 參數中所指定的對應值。



| 旗標                           | 意義                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| 堆積 \_ 無 \_ 序列化<br/> | 當 **RtlFreeHeap** 存取堆積時，不會使用相互排除。 <br/> |



 

</dd> <dt>

*HeapBase* \[在\]
</dt> <dd>

要釋放之記憶體區塊的指標。 [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)會傳回這個指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功釋放區塊，則傳回 **TRUE** ;否則 **為 FALSE** 。

> [!Note]  
> 從 Windows 8 開始，傳回值的類型為 **LOGICAL**，其大小與 **布林** 值不同。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                    |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| 標頭<br/>                   | <dl> <dt>Ntifs (包含 Ntifs) </dt> </dl>                                    |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
