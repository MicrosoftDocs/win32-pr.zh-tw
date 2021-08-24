---
title: 'Caption 屬性 (Command 物件) '
description: 瞭解 Command 物件的 Caption 屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be282591a6ed59993239bfd37baa639c4c2572ba54db6d1e46118ed98e317fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726158"
---
# <a name="caption-property-command-object"></a>Caption 屬性 (Command 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

決定在指定的字元快顯功能表中針對 [**命令**](/windows/desktop/lwef/the-command-object) 顯示的文字。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_*_"。標題_ *  \[  =  *字串*\]



| 部分     | 描述                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | 評估為顯示為 **命令** 標題之文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。

如果您未定義命令的 **VoiceCaption** ，則會使用您的 **標題** 設定。

 

 
