---
title: 'FontSize 屬性 (命令物件) '
description: 瞭解 FontSize 命令物件屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cee9d4852a68792fe1270ebd9c91e51f567adc546433d7142de68392e9f8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751431"
---
# <a name="fontsize-property-commands-object"></a>FontSize 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




