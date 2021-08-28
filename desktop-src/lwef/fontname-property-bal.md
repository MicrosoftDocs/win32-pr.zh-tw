---
title: 'FontName 屬性 (Balloon 物件) '
description: 瞭解 FontName Balloon 物件屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17ac59e1e11575ddf4144c90d122096c24542ee28130552eff0ba53ed4af17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349228"
---
# <a name="fontname-property-balloon-object"></a>FontName 屬性 (Balloon 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定指定字元之文字批註中所使用的字型。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) 。FontName_ *  \[  =  *字型*\]



| 部分   | 描述                                      |
|--------|--------------------------------------------------|
| *字體* | 對應至字型名稱的字串值。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**FontName**](fontname-property.md)屬性會定義用來在字串的文字氣球視窗中顯示文字的字型。 在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。 此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 如果您使用未編譯的字元，請檢查字元的 [**FontName**](fontname-property.md) 和 [**FontCharSet**](fontcharset-property.md) 屬性，以判斷它們是否適用于您的地區設定。 您可能必須先設定這些值，然後才能使用 [ [**朗讀**](speak-method.md) ] 方法，以確保文字顯示在 [文字] 氣球內的適當文字。

 

 

 




