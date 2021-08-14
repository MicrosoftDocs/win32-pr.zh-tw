---
title: '內容屬性 (字元物件) '
description: 深入瞭解字元物件的 [內容] 屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c790f4e3b0e69f4c8dc5e032b0021067e908f4af6200432dae668d08b47e1f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478715"
---
# <a name="helpcontextid-property-characters-object"></a>內容屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字元的相關聯內容編號。 用來為字元提供即時線上說明。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) 。_ *  \[  =  *值* 比\]



| 部分     | 描述                                   |
|----------|-----------------------------------------------|
| *Number* | 指定有效內容編號的整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

若要支援字元的即時線上說明，請在編譯說明檔時，將內容編號指派給您用於關聯說明主題的字元。 這個屬性只適用于字元的用戶端;此設定不會影響其他用戶端的字元或其他字元的用戶端。

如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md)則代理程式會在 [**HelpModeOn**](helpmodeon-property.md)設定為 **True** ，且使用者按一下該字元時，自動呼叫說明。 如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。 目前的內容編號是 **字元的 [值] 的值** 。

> [!Note]  
> 建立說明檔需要 Microsoft Windows help 編譯器。

 

## <a name="see-also"></a>另請參閱

[**內容説明屬性**](helpfile-property.md)


 

 




