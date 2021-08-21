---
title: WebHelp 方法
description: webHelp 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。 |WebHelp 方法
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- webHelp 方法 Windows Media Player
- webHelp 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，webHelp 方法
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577872"
---
# <a name="errorwebhelp-method"></a>WebHelp 方法

**webHelp** 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。

## <a name="syntax"></a>語法


```JScript
Error.webHelp()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

Web 說明頁面一律包含 Windows Media Player 錯誤的最新和最詳細的資訊。 此方法會自動傳送 Web 說明所需的其他資訊，例如使用的作業系統版本。

若要直接存取 Web 說明頁面，請使用下列錯誤碼和支援中心連結。

-   [Windows Media Player錯誤碼資訊](https://support.microsoft.com/kb/886273)
-   [Windows Media Player解決方案中心](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 元素，以啟動 Microsoft Windows Media Player Web 說明頁面。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Error 物件**](error-object.md)
</dt> </dl>

 

 





