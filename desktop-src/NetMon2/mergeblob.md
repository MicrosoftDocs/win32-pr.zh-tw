---
description: MergeBlob 函式會將來源 BLOB 中的所有專案複製到目的地 BLOB。
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: 'MergeBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943516"
---
# <a name="mergeblob-function"></a>MergeBlob 函式

**MergeBlob** 函式會將來源 blob 中的所有專案複製到目的地 blob。

## <a name="syntax"></a>語法


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDstBlob* \[in、out\]
</dt> <dd>

目的地 BLOB 的控制碼。 在輸入時，此 BLOB 包含其原始資訊。 在輸出中，此 BLOB 包含其原始資訊，以及來源 BLOB 的所有資訊。

</dd> <dt>

*hSrcBlob* \[在\]
</dt> <dd>

來源 BLOB 的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="remarks"></a>備註

來源和目的地檔案的通用專案將會以來源 BLOB 的資料覆寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




