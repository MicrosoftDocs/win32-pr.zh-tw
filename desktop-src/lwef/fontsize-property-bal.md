---
title: 'FontSize 屬性 (Balloon 物件) '
description: FontSize 屬性
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383722"
---
# <a name="fontsize-property-balloon-object"></a>FontSize 屬性 (Balloon 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

針對指定的字元，傳回或設定文字氣球所支援的字型大小。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. * * * 字元* * **( "**_CharacterID_*_" ) 。FontSize_* \[  =  *點*\]



| 部分     | 描述                                              |
|----------|----------------------------------------------------------|
| *點* | 長整數值，指定以點為單位的字型大小。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**FontSize**](fontsize-property.md)屬性會傳回長整數值，以點指定目前的字型大小。 **FontSize** 的最大值是2160點。

在 [Microsoft 代理程式字元編輯器] 中，會設定字元字提示字元之字型設定的預設值。 此外，使用者可以覆寫 Microsoft Agent 屬性工作表中所有字元的字型設定。

 

 




