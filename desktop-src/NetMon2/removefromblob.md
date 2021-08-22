---
description: RemoveFromBlob 函式會刪除任何層級的 BLOB 專案 (擁有者、類別或標記) 。
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: 'RemoveFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063688"
---
# <a name="removefromblob-function"></a>RemoveFromBlob 函式

**RemoveFromBlob** 函式會刪除任何層級的 BLOB 專案 (**擁有** 者、**類別** 或 **標記**) 。

## <a name="syntax"></a>語法


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

要從中刪除專案之 BLOB 的控制碼。

</dd> <dt>

*pOwnerName* \[在\]
</dt> <dd>

**擁有** 者名稱的指標。

</dd> <dt>

*pCategoryName* \[在\]
</dt> <dd>

**類別目錄** 名稱的指標。 **Null** 參數值表示呼叫端正在嘗試刪除指定的 **擁有** 者資訊及其所有子專案。 請注意，如果 *pCategoryName* 參數值為 **null**， *PTagName* 參數也必須是 **null**。

</dd> <dt>

*pTagName* \[在\]
</dt> <dd>

**標記** 名稱的指標。 **Null**_pTagName_ 值表示呼叫端正在嘗試刪除指定的 **類別** 及其所有子專案。 如果參數值不是 **Null**，則呼叫端會要求只刪除指定的 **標記** 專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




