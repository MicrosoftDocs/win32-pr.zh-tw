---
title: FramesSkipped
description: FramesSkipped 屬性會抓取播放期間略過的總畫面格數。
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- FramesSkipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989861"
---
# <a name="networkframesskipped"></a>FramesSkipped

**FramesSkipped** 屬性會抓取播放期間略過的總畫面格數。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**framesSkipped**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**framesSkipped** 可顯示當使用者按一下按鈕時，播放期間略過的框架總數。 這項資訊會顯示在以 ID = "FS" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> </dl>

 

 





