---
title: 儲存體和資料流程
description: 儲存物件類似于檔案系統目錄。
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671768"
---
# <a name="storages-and-streams"></a>儲存體和資料流程

儲存物件類似于檔案系統目錄。 就像目錄可以包含其他目錄和檔案一樣，儲存物件也可以包含其他儲存物件和資料流程物件。 和目錄一樣，儲存物件也會追蹤儲存物件的位置和大小，以及在其底下嵌套的資料流程物件。

資料流程物件類似于傳統的檔案概念。 就像檔案一樣，資料流程所包含的資料會儲存為連續的位元組序列。

COM 複合檔案是由根儲存物件所組成，其中至少包含一個代表其原生資料的資料流程物件，以及一個或多個對應至其連結與内嵌物件的儲存物件。 根儲存物件會對應到它所發生之任何檔案系統中的檔案名。 檔中的每個物件也會以包含一或多個資料流程物件的儲存物件表示，也可能包含一或多個儲存物件。 如此一來，檔可以包含不限數目的嵌套物件。 如需詳細資訊，請參閱 [複合檔案](compound-files.md)。

 

 




