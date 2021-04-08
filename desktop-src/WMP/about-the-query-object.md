---
title: 關於 Query 物件
description: 關於 Query 物件
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player，Query 物件
- Windows Media Player 物件模型、Query 物件
- 物件模型、查詢物件
- Windows Media Player ActiveX 控制項、Query 物件
- ActiveX 控制項、Query 物件
- Windows Media Player Mobile ActiveX 控制項、Query 物件
- Windows Media Player Mobile、Query 物件
- Query 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673395"
---
# <a name="about-the-query-object"></a>關於 Query 物件

**查詢** 物件代表複合查詢。 您可以藉由呼叫 *mediaCollection* 來建立新的空白 **查詢** 物件。**createQuery**。 建立 **查詢** 物件之後，您可以呼叫 **addCondition** 將條件加入至複合查詢。 後續每次呼叫 **addCondition** 時，會使用和邏輯，將新的條件附加至現有的查詢。

例如，假設您想要建立一個查詢，以代表所有數位媒體，其中 **WM/** 類型等於「爵士樂」且 **作者** 包含「Jim」。 您可以使用下列 JScript 程式碼，建立複合查詢來表示這些條件：


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



若要使用或邏輯將條件加入至複合查詢，您必須呼叫 **beginNextGroup**。 這個方法會指出先前的條件群組已完成，而且下一次呼叫 **addCondition** 時，代表新條件群組的開始。

例如，若要建立代表所有數位媒體的查詢，其中 **WM/** 類型等於「爵士樂」且 **作者** 包含 "Jim" 或 **作者** 包含 "Dave"，您可以使用下列範例程式碼：


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



若要執行複合查詢，請呼叫 **MediaCollection. getPlaylistByQuery**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Query 物件**](query-object.md)
</dt> </dl>

 

 




