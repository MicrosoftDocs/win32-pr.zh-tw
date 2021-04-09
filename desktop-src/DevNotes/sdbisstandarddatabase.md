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
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025813"
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



 

 




