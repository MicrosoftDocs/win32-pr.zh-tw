---
description: BuildINIPath 函式會傳回 INI 檔案的完整路徑，該檔案會對應到您輸入的資訊。
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: 'BuildINIPath 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744688"
---
# <a name="buildinipath-function"></a>BuildINIPath 函式

**BuildINIPath** 函式會傳回 INI 檔案的完整路徑，該檔案會對應到您輸入的資訊。

## <a name="syntax"></a>語法


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FullPath* 
</dt> <dd>

接收完整 INI 檔案名的緩衝區。

</dd> <dt>

*IniFileName* 
</dt> <dd>

INI 檔案名 (檔案名減去副檔名) 的完整檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是完整 INI 檔案名的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

此函式傳回的路徑是與您輸入的資訊對應之 INI 檔案的完整路徑。 例如，如果您輸入 XNS 或 TCP，函數會分別產生 Xns.ini 或 Tcp.ini 的路徑。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




