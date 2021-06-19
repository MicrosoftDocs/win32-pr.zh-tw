---
title: 'Width 屬性 (字元物件) '
description: 深入瞭解字元物件的 Width 屬性，它會針對指定的字元傳回或設定框架的寬度。
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395124"
---
# <a name="width-property-characters-object"></a>Width 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定指定字元的框架寬度。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。寬度_ *  \[ =  *值*\]



| 部分    | 描述                                                |
|---------|------------------------------------------------------------|
| *value* | 指定字元框架寬度的長整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**Width**](width-property.md)屬性一律以圖元表示。 這個屬性的設定會套用到字元的所有用戶端。

雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。

 

 




