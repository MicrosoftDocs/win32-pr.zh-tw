---
description: 從指定的資料庫抓取指定之標記和索引鍵類型的索引。
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468201"
---
# <a name="sdbgetindex-function"></a>SdbGetIndex 函式

從指定的資料庫抓取指定之標記和索引鍵類型的索引。

## <a name="syntax"></a>語法


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tWhich* \[在\]
</dt> <dd>

標記。

</dd> <dt>

*tKey* \[在\]
</dt> <dd>

索引鍵類型。

</dd> <dt>

*lpdwFlags* \[out、optional\]
</dt> <dd>

此參數可以是0或 **SHIMDB \_ 索引 \_ 唯一索引 \_ 鍵** (0x00000001) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

索引的 **TAGID** 或 **TAGID \_ Null**。

## <a name="remarks"></a>備註

產生的索引可用於讀取作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




