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
ms.openlocfilehash: ec2acf733a870d3dcff57ceb7cdea996c6b6dc1e5d950ec85944285e6ba6cc35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815138"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




