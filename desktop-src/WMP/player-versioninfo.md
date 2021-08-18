---
title: VersionInfo
description: VersionInfo 屬性會捕獲指定 Windows Media Player 版本的字串值。
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- VersionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995828"
---
# <a name="playerversioninfo"></a>VersionInfo

**VersionInfo** 屬性會捕獲指定 Windows Media Player 版本的字串值。

## <a name="syntax"></a>Syntax

*玩家* 。**versionInfo**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，格式如下： "*X*. 0.0。*Yyyy*」，其中 *X* 代表主要版本號碼，而 *yyyy* 代表組建編號。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，按此按鈕時，會顯示訊息方塊，其中包含 Windows Media Player 的版本資訊。 使用 ID = "Player" 建立 **player** 物件。


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





