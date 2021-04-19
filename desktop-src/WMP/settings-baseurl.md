---
title: 設定. baseURL
description: BaseURL 屬性會指定或抓取基底 URL，這個基底 URL 使用內嵌在媒體專案中的 URL 指令碼命令來解析相對路徑。
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- 設定. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994183"
---
# <a name="settingsbaseurl"></a>設定. baseURL

**BaseURL** 屬性會指定或抓取基底 URL，這個基底 url 使用內嵌在媒體專案中的 URL 指令碼命令來解析相對路徑。

## <a name="syntax"></a>Syntax

baseURL

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這個屬性會指定 **ScriptCommand** 事件以命令參數形式傳遞的基底 HTTP URL。 基底 URL 會與相對 URL 串連，如下所示：

1.  尾端正斜線 (/) 會新增至 **baseURL** 屬性的值。
2.  前置句點、反斜線或正斜線 (.、 \\ 和/) 會從相對 URL 中刪除。
3.  相對 URL 會新增至基底 URL 的結尾。
4.  產生的完整 URL 中的所有斜線都會指向相同方向 (轉換成正斜線或反斜線) 根據新 URL 中遇到的第一個斜線字元的方向。

**注意**

播放機控制項不支援使用兩個期間 (。在相對 URL 中 ) ，表示目前位置的父系。

**Windows Media Player 10** 行動裝置版：此屬性是唯讀的，而且一律會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ScriptCommand 事件**](player-player-scriptcommand.md)
</dt> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





