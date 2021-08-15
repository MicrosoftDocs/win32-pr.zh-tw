---
title: " (舊版 Windows 環境功能的 Play 方法) "
description: Play 方法
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980c13cbf11e86a25485558fb3ff2ade703010eb180e86291f206ea152f3c0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247084"
---
# <a name="play-method-legacy-windows-environment-features"></a> (舊版 Windows 環境功能的 Play 方法) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

針對指定的字元播放指定的動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。Play_* "*AnimationName*"

</dd> </dl> 

| 部分            | 描述                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | 必要。 指定動畫順序名稱的字串。 |



 

## <a name="remarks"></a>備註

使用 Microsoft Agent 字元編輯器來編譯字元時，會定義動畫的名稱。 在播放指定的動畫之前，伺服器會嘗試播放先前 **動畫的傳回動畫（** 如果已指派）。

使用傳統檔案通訊協定來存取字元的動畫時，您可以直接使用 **Play** 方法指定動畫的名稱。 但是，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **Play** 方法之前，使用 **Get** 方法載入動畫。

如需詳細資訊，請參閱 **Get** 方法。

若要簡化您的語法，您可以宣告物件參考，並將它設定為參考 [**字元**](/windows/desktop/lwef/the-characters-object)集合中的 [**字元**](/windows/desktop/lwef/the-characters-object)物件，並使用參考作為 **播放** 語句的一部分：


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果您指定未載入的動畫或未成功載入該字元，伺服器會將 **要求** 物件的 [**Status**](status-property.md)屬性設為「失敗」，並提供適當的錯誤號碼。 但是，如果動畫不存在，且已成功載入字元的資料，伺服器就會引發錯誤。

**Play** 方法不會讓字元變成可見。 如果看不到字元，伺服器會以不可見的狀態播放動畫，並設定 [**Request**](/windows/desktop/lwef/the-request-object)物件的 [**Status**](status-property.md)屬性。

 

 
