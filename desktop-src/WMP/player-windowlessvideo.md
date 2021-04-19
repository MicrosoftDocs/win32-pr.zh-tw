---
title: WindowlessVideo
description: WindowlessVideo 屬性會指定或抓取值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- WindowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990049"
---
# <a name="playerwindowlessvideo"></a>WindowlessVideo

**WindowlessVideo** 屬性會指定或抓取值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。

## <a name="syntax"></a>Syntax

*玩家*。**windowlessVideo**

## <a name="possible-values"></a>可能的值

這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。



| 值 | 描述                                      |
|-------|--------------------------------------------------|
| true  | 影片以無視窗模式呈現。        |
| false | 預設值。 影片會以視窗模式呈現。 |



 

## <a name="remarks"></a>備註

根據預設，內嵌的 Windows Media Player 控制項會在用戶端區域內的它自己的視窗中呈現影片。 當 **windowlessVideo** 設定為 true 時，播放程式控制項會直接在工作區中轉譯影片，因此您可以套用特殊效果或以文字將影片分層。

在 Windows Vista 中，以無視窗模式轉譯影片可能會降低效能。

Netscape Navigator 不支援 **windowlessVideo** 屬性。 在 [導覽器] 中設定此屬性的值可能會產生非預期的結果。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player。<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





