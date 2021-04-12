---
description: 開啟指定的 Apphelp 詳細資料資料庫。
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109916"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>SdbOpenApphelpDetailsDatabase 函式

開啟指定的 Apphelp 詳細資料資料庫。

## <a name="syntax"></a>語法


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwsDetailsDatabasePath* \[在中，選擇性\]
</dt> <dd>

資料庫路徑。 如果此參數為 **Null**，則會開啟本機系統資料庫。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 Apphelp details 資料庫的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




