---
title: 'Caption 屬性 (命令集合物件) '
description: 瞭解命令集合物件的 Caption 屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976698"
---
# <a name="caption-property-commands-collection-object"></a>Caption 屬性 (命令集合物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

決定在字元的快顯功能表中針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件顯示的文字。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。_ *[命令。標題](caption-property.md) \[  =  *字串*\]



| 部分     | 描述                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | 評估為顯示為標題之文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性，可定義當其 [**Visible**](visible-property.md)屬性設定為 True 且您的應用程式不是輸入-主動用戶端時，它會在字元的快顯功能表上顯示的方式。 若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。

如果您針對具有 [**標題**](caption-property.md)的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合定義命令，您通常也會為其相關聯的 **命令** 集合定義 **標題**。

 

 
