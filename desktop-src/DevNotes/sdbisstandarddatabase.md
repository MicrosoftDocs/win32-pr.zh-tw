---
description: 判斷指定的資料庫是否為其中一個標準資料庫 (Sysmain、Apphelp、Drvmain 或 Msimain) 。
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045188"
---
# <a name="sdbisstandarddatabase-function"></a>SdbIsStandardDatabase 函式

判斷指定的資料庫是否為其中一個標準資料庫 (Sysmain、Apphelp、Drvmain 或 Msimain) 。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*GuidDB* \[在\]
</dt> <dd>

資料庫的 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 GUID 代表標準資料庫，則函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




