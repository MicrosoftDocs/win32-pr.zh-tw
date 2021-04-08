---
description: UIText 資料表包含使用者介面中使用之部分字串的當地語系化版本。 這些字串不是任何其他資料表的一部分。 UIText 資料表適用于任何其他資料表中沒有邏輯位置的字串。
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: UIText 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111984"
---
# <a name="uitext-table"></a>UIText 資料表

UIText 資料表包含使用者介面中使用之部分字串的當地語系化版本。 這些字串不是任何其他資料表的一部分。 UIText 資料表適用于任何其他資料表中沒有邏輯位置的字串。

UIText 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 答案    | [識別碼](identifier.md) | Y   | N        |
| Text   | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

識別特定字串的唯一索引鍵。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

字串的當地語系化版本。

</dd> </dl>

## <a name="remarks"></a>備註

某些控制項使用 UIText 資料表作為字串的來源。 如需此表中每個特定控制項所需之字串的相關資訊，請參閱 [消費者介面參考](user-interface-reference.md)中的個別控制項。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



