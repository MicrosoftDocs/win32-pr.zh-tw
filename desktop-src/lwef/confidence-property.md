---
title: 信賴屬性
description: 信賴屬性
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375037"
---
# <a name="confidence-property"></a>信賴屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定用戶端的 **信賴度** 是否出現在接聽提示中。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 (***"CharacterID ***" ) 的字元。命令 ( "*** name ***" )**. * * 信賴* *  \[  =  *號碼*\]



| 部分     | 描述                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Number* | 評估為長整數的數值運算式，可識別 [**命令**](/windows/desktop/lwef/the-command-object)的信賴值。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果最符合的傳回信賴值 (Userinput>。信賴) 不會超過您為 **信賴** 屬性設定的值，則 [**ConfidenceText**](confidencetext-property.md) 中提供的文字會顯示在接聽提示中。

 

 