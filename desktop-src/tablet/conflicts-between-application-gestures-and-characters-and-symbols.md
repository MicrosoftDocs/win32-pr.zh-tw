---
description: 應用程式手勢和字元和符號之間的衝突描述。
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: 應用程式手勢和字元和符號之間的衝突
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971992"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>應用程式手勢和字元和符號之間的衝突

有些應用程式手勢可能與字元、字元組合、字元和符號組合或以單一筆劃撰寫的全字組相衝突。 您可以對執行應用程式手勢的內容有詳細的瞭解，以避免這些衝突的大部分。

例如，若要區分右邊的手勢與虛線 ( ) 或底線 (\_) ，應用程式可能會篩選出手勢對相鄰字元的距離、相對於字元的相對大小，或封包中包含的其他資訊。 應用程式手勢的時間也可能是決定手勢和字元之間的決定因素。 套用應用程式手勢之前可能會有更多暫停，而不是在輸入字元之前。 除非使用者正在執行一系列的復原或倒退鍵手勢，否則筆勢之後可能也會有更多的暫停，而不是字元。

下列主題將詳細說明這些衝突：

-   [與拉丁字元和符號衝突](conflicts-with-latin-characters-and-symbols.md)
-   [與 East-Asian 字元衝突](conflicts-with-east-asian-characters.md)

 

 



