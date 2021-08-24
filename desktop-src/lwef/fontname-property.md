---
title: 'FontName 屬性 (命令物件) '
description: 瞭解 FontName 命令物件屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f8c9c66e7d205e79a3ac9b076fa4e01852df358657761f8792d42b764b270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725708"
---
# <a name="fontname-property-commands-object"></a>FontName 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定在字元的快顯功能表中使用的字型。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . FontName_ *  \[  =  *字型*\]



| 部分   | 描述                                      |
|--------|--------------------------------------------------|
| *Font* | 對應至字型名稱的字串值。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**FontName** 屬性會定義在字元的快顯功能表中用來顯示文字的字型。 字型設定的預設值是以字元的 **LanguageID** 設定的功能表字型設定為基礎，如果未設定則為---使用者預設語言識別項設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

 

 




