---
title: 'FontSize 屬性 (命令物件) '
description: FontSize 屬性
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106984950"
---
# <a name="fontsize-property-commands-object"></a>FontSize 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定在字元的快顯功能表中使用的字型大小。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) . FontSize_ *  \[  =  *點*\]



| 部分     | 描述                                              |
|----------|----------------------------------------------------------|
| *點* | 長整數值，指定以點為單位的字型大小。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**FontSize** 屬性會定義用來在字元的快顯功能表中顯示文字的字型的點大小。 字型設定的預設值是以字元 **LanguageID** 設定的功能表字型設定為基礎，或者，如果未設定，則是使用者預設語言設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

 

 




