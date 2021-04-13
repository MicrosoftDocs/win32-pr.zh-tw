---
title: ConfidenceText 屬性
description: ConfidenceText 屬性
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375164"
---
# <a name="confidencetext-property"></a>ConfidenceText 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定出現在接聽提示中的用戶端 **ConfidenceText** 。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

* 代理程式 ***。 (***"CharacterID ***" ) 的字元。命令 ( "*** name ***" )**。 \[ ConfidenceText  = *字串*\]



| 部分     | 描述                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | 評估為 [**命令**](/windows/desktop/lwef/the-command-object)之 **ConfidenceText** 文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

當最符合 (Userinput> 的信賴) 不超過 [**信賴**](confidence-property.md) 設定時，伺服器會在接聽提示中顯示在 **ConfidenceText** 中提供的文字。

 

 