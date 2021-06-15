---
title: 'Height 屬性 (字元物件) '
description: 深入瞭解字元物件的 Height 屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068507"
---
# <a name="height-property-characters-object"></a>Height 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定指定之字元框架的高度。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。高度_ *  \[ =  *值*\]



| 部分    | 描述                                                 |
|---------|-------------------------------------------------------------|
| *value* | 指定字元之框架高度的長整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**Height** 屬性一律會以圖元表示（相對於螢幕座標 (左上) ）。 這個屬性的設定會套用到字元的所有用戶端。

雖然字元會出現在不規則形狀的區域視窗中，但字元的高度是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。

 

 




