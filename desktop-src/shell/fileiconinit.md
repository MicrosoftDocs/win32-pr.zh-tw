---
description: 初始化或重新初始化系統映射清單。
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111808"
---
# <a name="fileiconinit-function"></a>FileIconInit 函式

初始化或重新初始化系統映射清單。

## <a name="syntax"></a>語法


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fRestoreCache* \[在\]
</dt> <dd>

類型： **BOOL**

**TRUE** 表示從磁片還原系統映射快取;否則 **為 FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果已成功重新整理快取，**則為 TRUE** ，如果初始化失敗，則為 **FALSE** 。

## <a name="remarks"></a>備註

如果您在自己的進程中使用系統映射清單，您必須在下列時間呼叫 **FileIconInit** ：

-   啟動時。
-   在設定 [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)旗標時回應 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md)訊息。

**FileIconInit** 不包含在標頭檔中。 您必須直接從 Shell32.dll 使用序數660來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
