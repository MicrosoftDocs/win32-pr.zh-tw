---
title: 'VoiceCaption 屬性 (命令物件) '
description: 瞭解命令物件的 VoiceCaption 屬性，此屬性會傳回或設定 [語音命令] 視窗中針對命令物件顯示的文字。
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b753a1f76769a6d6ec28de3161d01a097108c0c3f973f78e397f1c764fba8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358728"
---
# <a name="voicecaption-property-commands-object"></a>VoiceCaption 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定 [語音命令] 視窗中針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件顯示的文字。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . VoiceCaption_ *  \[  =  *字串*\]



| 部分     | 描述                                               |
|----------|-----------------------------------------------------------|
| *string* | 評估為顯示之文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性，您通常也會設定其 **VoiceCaption** 屬性。 當您的用戶端應用程式為輸入-使用中且字元可見時，[ **VoiceCaption** 文字] 設定就會出現在 [語音命令] 視窗中。 如果未設定這個屬性， **命令** 集合的 [**Caption**](caption-property.md) 屬性的設定會決定顯示的文字。 未設定 **VoiceCaption** 或 **Caption** 屬性時，當用戶端應用程式變成輸入主動時，集合中的命令會出現在 [ (未定義的命令) ] 下的 [語音命令] 視窗中。

**VoiceCaption** 設定也會決定要在接聽提示中顯示的文字，以指出該字元接聽的命令。

## <a name="see-also"></a>另請參閱

[Caption 屬性](caption-property.md)


 

 
