---
description: 類別可協助您組織事件，讓事件檢視器可以進行篩選。 每個事件來源都可以定義自己的編號類別以及它們所對應的文字字串。
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: 事件類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d68895c1043e12ab8e53e3d6db8cd385d17ccc0175c5610a487682fc1c92c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151639"
---
# <a name="event-categories"></a>事件類別

類別可協助您組織事件，讓事件檢視器可以進行篩選。 每個 [事件來源](event-sources.md) 都可以定義自己的編號類別以及它們所對應的文字字串。

類別必須連續編號，以數位1為開頭。 類別本身會定義在訊息檔案中。 例如，使用下列語法來宣告三個事件類別目錄。 在事件檢視器中，使用這些分類的事件將會在 [ **類別目錄** ] 資料行中顯示類別1、類別2或類別3。

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

類別可以儲存在個別的訊息檔案中，或是儲存在包含其他類型訊息的檔案中。 如果您建立單一訊息檔案，請確定類別是檔案中的第一則訊息。 如需建立和使用訊息檔案的詳細資訊，請參閱 [訊息](message-files.md)檔。

類別目錄總數會儲存在事件來源的 **CategoryCount** 值中。

 

 



