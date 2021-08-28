---
title: ConfidenceText 屬性
description: ConfidenceText 屬性
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6612d4ade657748674fb4dd7391f447849691dcd756f2320f590c00ac33430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963148"
---
# <a name="confidencetext-property"></a>ConfidenceText 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定出現在接聽提示中的用戶端 **ConfidenceText** 。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。字元 ( "**_CharacterID_*_" ) . 命令 ( "_*_name_*_" )_*。 \[ ConfidenceText  = *字串*\]



| 部分     | 描述                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | 評估為 [**命令**](/windows/desktop/lwef/the-command-object)之 **ConfidenceText** 文字的字串運算式。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

當最符合 (Userinput> 的信賴) 不超過 [**信賴**](confidence-property.md) 設定時，伺服器會在接聽提示中顯示在 **ConfidenceText** 中提供的文字。

 

 