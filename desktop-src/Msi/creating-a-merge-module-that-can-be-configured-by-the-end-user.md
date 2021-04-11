---
description: 若要建立合併模組，請使用「撰寫合併模組」主題中所述的一般方針。
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: 建立可由 End-User 設定的合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193503"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>建立可由 End-User 設定的合併模組

若要建立合併模組，請使用「 [撰寫合併模組](authoring-merge-modules.md) 」主題中所述的一般方針。 此外，您必須執行下列動作，才能建立可由模組的終端使用者設定的合併模組：

-   終端使用者必須有 Mergemod.dll 版本2.0 才能設定您的模組。 具有舊版 Mergemod.dll 的使用者可以套用模組，但一律會取得預設設定。
-   將 [ModuleConfiguration 資料表](moduleconfiguration-table.md) 加入至合併模組，以識別使用者可能設定的專案。 為每個可設定的專案新增此資料表中的記錄。 這些專案會取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)中所指定的範本。 在 [名稱] 欄位中輸入每個可設定專案的名稱。 針對 [格式]、[類型] 和 [CoNtextData] 資料行中的每個專案，輸入格式、類型和語義內容。 如需詳細資訊，請參閱 [語義類型](semantic-types.md)。 使用 [CMSM 的特殊格式](cmsm-special-format.md)，在 [DefaultValue] 欄位中輸入專案的預設值。
-   將 [ModuleSubstitution 資料表](modulesubstitution-table.md) 加入至合併模組。 這個資料表中的每一筆記錄都會對應到一個或多個可設定的專案，並放入 merge module 資料庫的一個欄位中。 輸入接收替代之欄位的資料表、資料列和資料行。 使用 [CMSM 的特殊格式](cmsm-special-format.md)，在 [值] 資料行中輸入替代的格式設定範本。
-   將記錄加入至 ModuleSubstitution 和 ModuleConfiguration 資料表的 [驗證資料表](-validation-table.md) 。
-   將記錄加入至[ModuleSubstitution 資料表](modulesubstitution-table.md)和[ModuleConfiguration 資料表](moduleconfiguration-table.md)的[ModuleIgnoreTable 資料表](moduleignoretable-table.md)。 這可確保模組與版本為2.0 的 Mergemod.dll 版本的使用者相容。

 

 



