---
title: PlayerApplication.playerDocked
description: PlayerDocked 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。
ms.assetid: c6f82188-0826-4854-992c-85ad84701fb7
keywords:
- PlayerApplication. playerDocked Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.playerDocked
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c53ac92aac82c19dd9e58d389dee340a5951457b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979439"
---
# <a name="playerapplicationplayerdocked"></a>PlayerApplication.playerDocked

**PlayerDocked** 屬性會抓取值，指出 Windows Media Player 是否處於停駐狀態。

## <a name="syntax"></a>Syntax

*playerApplication*。**playerDocked**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。

## <a name="remarks"></a>備註

只有在遠端處理 Windows Media Player 控制項時，才會使用這個屬性。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayerApplication 物件**](playerapplication-object.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





