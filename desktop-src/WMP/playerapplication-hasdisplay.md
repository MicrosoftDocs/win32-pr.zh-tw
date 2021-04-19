---
title: PlayerApplication.hasDisplay
description: HasDisplay 屬性會抓取值，指出影片是否可以透過遠端播放機控制項來顯示。
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000767"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

**HasDisplay** 屬性會抓取值，指出影片是否可以透過遠端播放機控制項來顯示。

## <a name="syntax"></a>Syntax

*playerApplication*。**hasDisplay**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。

## <a name="remarks"></a>備註

只有在遠端處理 Windows Media Player 控制項時，才會使用這個屬性。

您可以同時在遠端執行數個 Windows Media Player 控制項，但在播放程式的完整模式或其中一個遠端 Windows Media Player 控制項中，影片一次只能顯示在一個位置。 您可以使用這個屬性來判斷目前的控制項是否為可顯示影片的控制項。

**Windows Media Player 10** 行動裝置版：這個屬性一律會傳回 **true**。

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

 

 





