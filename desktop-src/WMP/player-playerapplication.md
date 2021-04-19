---
title: PlayerApplication
description: 當遠端 Windows Media Player 控制項正在執行時，playerApplication 屬性會捕獲 PlayerApplication 物件。
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- PlayerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994682"
---
# <a name="playerplayerapplication"></a>PlayerApplication

當遠端 Windows Media Player 控制項正在執行時， **playerApplication** 屬性會捕獲 **playerApplication** 物件。

## <a name="syntax"></a>Syntax

**playerApplication**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **PlayerApplication** 物件或 null 值。

## <a name="remarks"></a>備註

只有在遠端處理 Windows Media Playercontrol 時，才會使用這個屬性。 如果值為 null，則不會在遠端模式中內嵌 Windows Media Playercontrol。

這個屬性只能在 c + + 程式碼中存取，或透過 playerApplication 全域變數在外觀的腳本中存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**全域屬性**](global-attributes.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlayerApplication 物件**](playerapplication-object.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





