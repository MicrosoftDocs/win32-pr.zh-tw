---
title: '內容屬性 (命令集合物件) '
description: 瞭解命令集合物件的 [上下文] 屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0635f62350d0bea31afda09b04e6489fe7f0ccb33173adb6c2aeb69a814265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725698"
---
# <a name="helpcontextid-property-commands-collection-object"></a>內容屬性 (命令集合物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件的相關聯內容編號。 用來提供 **命令** 物件的即時線上說明。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . 命令 ( "_*_name_*_" ) 。_ *  \[  =  *值* 比\]



| 部分     | 描述                                   |
|----------|-----------------------------------------------|
| *Number* | 指定有效內容編號的整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md)則代理程式會在 [**HelpModeOn**](helpmodeon-property.md)設定為 **True** 且使用者選取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)物件時，自動呼叫說明。 如果您在 [協助工具] 中設定內容編號，Agent 會呼叫 [說明 **]，並** 搜尋該內容編號所識別的主題。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 建立說明檔需要 Microsoft Windows help 編譯器。

 

## <a name="see-also"></a>另請參閱

[**內容説明屬性**](helpfile-property.md)


 

 
