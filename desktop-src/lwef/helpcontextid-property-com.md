---
title: '內容屬性 (命令物件) '
description: '[上下文] 屬性'
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093704"
---
# <a name="helpcontextid-property-command-object"></a>內容屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的相關聯內容編號。 用來提供 **命令** 物件的即時線上說明。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . 命令 ( "" ) 。_ *  \[  =  *值* 比\]



| 部分     | 描述                                   |
|----------|-----------------------------------------------|
| *Number* | 指定有效內容編號的整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您已建立應用程式的 Windows 說明檔，並將字元的 [ [**檔案説明] 屬性設定**](helpfile-property.md) 為檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，代理程式會自動呼叫說明。 如果您在 [協助工具] 中設定內容編號，Agent 會呼叫 [說明 [**]，並**](helpcontextid-property.md)搜尋目前內容編號所識別的主題。 目前的內容編號是 **命令的值** 為的值。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 建立說明檔需要 Microsoft Windows 說明編譯器。

 

## <a name="see-also"></a>另請參閱

[**內容説明屬性**](helpfile-property.md)


 

 
