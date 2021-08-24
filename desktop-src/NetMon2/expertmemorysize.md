---
description: ExpertMemorySize 函數會傳回 ExpertAllocMemory 函數所配置的記憶體數量。
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: 'ExpertMemorySize 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744268"
---
# <a name="expertmemorysize-function"></a>ExpertMemorySize 函式

**ExpertMemorySize** 函數會傳回 [ExpertAllocMemory](expertallocmemory.md)函數所配置的記憶體數量。

## <a name="syntax"></a>語法


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

獨特的專家識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*pOriginalMemory* \[在\]
</dt> <dd>

[ExpertAllocMemory](expertallocmemory.md)所配置專家的記憶體位址指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回配置的記憶體數量（以位元組為單位）。

## <a name="remarks"></a>備註

如需 **ExpertMemorySize** 所傳回之 **大小 \_ T** 資料類型的相關資訊，請參閱資料類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




