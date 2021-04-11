---
description: 將指定檔案中的二進位資料寫入至指定的資料庫。
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936188"
---
# <a name="sdbwritebinarytagfromfile-function"></a>SdbWriteBinaryTagFromFile 函式

將指定檔案中的二進位資料寫入至指定的資料庫。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tTag* \[在\]
</dt> <dd>

專案的標記。 這個標記必須是 **標記 \_ 類型 \_ BINARY** 類型。

</dd> <dt>

*pwszPath* \[在\]
</dt> <dd>

包含資料之檔案的路徑。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




