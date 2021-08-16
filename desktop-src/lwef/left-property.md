---
title: 'Left 屬性 (字元物件) '
description: 深入瞭解 [左字元] 物件屬性。 Microsoft 代理程式已于 Windows 7 淘汰。
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105014"
---
# <a name="left-property-characters-object"></a>Left 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定指定之字元框架的左邊緣。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。左_ *  \[  =  *值*\]



| 部分    | 描述                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | 指定字元框架左邊緣的長整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**左邊** 的屬性一律以圖元表示，相對於螢幕原點 (左上) 。 這個屬性的設定會套用到字元的所有用戶端。

雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。

 

 




