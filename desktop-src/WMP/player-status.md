---
title: 播放。狀態
description: Status 屬性會抓取值，指出 Windows Media Player 的狀態。
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. 狀態 Windows Media Player
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986182"
---
# <a name="playerstatus"></a>播放。狀態

**Status** 屬性會抓取值，指出 Windows Media Player 的狀態。

## <a name="syntax"></a>Syntax

*玩家* 。**狀態**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀字串。

## <a name="remarks"></a>備註

這個屬性中包含的值隨時可能會變更，而且僅供顯示之用。

每當這個屬性變更值時，就會引發 **StatusChange** 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 或更新版本。<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**StatusChange 事件**](player-player-statuschange.md)
</dt> </dl>

 

 





