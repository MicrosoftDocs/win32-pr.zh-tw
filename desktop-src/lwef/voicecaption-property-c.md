---
title: 'VoiceCaption 屬性 (Command 物件) '
description: 瞭解 Command 物件的 VoiceCaption 屬性，此屬性會設定或傳回 [語音命令] 視窗中針對命令物件顯示的文字。
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396163"
---
# <a name="voicecaption-property-command-object"></a>VoiceCaption 屬性 (Command 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

設定或傳回 [語音命令] 視窗中針對 [**命令**](/windows/desktop/lwef/the-command-object) 物件顯示的文字。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . 命令 ( "_*_Name_*_" ) 。VoiceCaption_ *  \[  =  *字串*\]



| 部分     | 描述                                               |
|----------|-----------------------------------------------------------|
| *string* | 評估為顯示之文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您在 [**命令**](https://www.bing.com/search?q=**Commands**)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。 當您的用戶端應用程式為輸入-使用中且字元可見時，此文字會出現在 [語音命令] 視窗中。 如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。 未設定 **VoiceCaption** 或 **Caption** 屬性時，命令不會出現在 [語音命令] 視窗中。

### <a name="see-also"></a>另請參閱

[**Caption 屬性**](caption-property.md)


 

 
