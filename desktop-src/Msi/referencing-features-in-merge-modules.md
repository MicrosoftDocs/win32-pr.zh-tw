---
description: 合併模組只會操作元件，而不會使用功能。 不過，合併模組中的某些資料表（例如 PublishComponent 資料表）包含參考特徵的欄位。
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: 參考合併模組中的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2857b71fd651955319457092d9cf689ded954af758e7906b44a761dfa6ad782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375948"
---
# <a name="referencing-features-in-merge-modules"></a>參考合併模組中的功能

合併模組只會操作元件，而不會使用功能。 不過，合併模組中的某些資料表（例如 [PublishComponent 資料表](publishcomponent-table.md)）包含參考特徵的欄位。

Null GUID： {00000000-0000-0000-0000-000000000000} 必須撰寫到參考功能之 merge module 資料庫的任何欄位中。 合併模組合併為安裝套件時，合併工具會將 null GUID 取代為安裝套件中指定的功能，但需要特殊處理的資料表除外，例如 [ModuleSignature 資料表](modulesignature-table.md) 和 ModuleSequence 資料表。

請注意，如果使用 null GUID 做為主鍵，則不保證合併工具所取代的值是唯一的。 合併模組的作者負責確保當合併工具將 null Guid 取代為功能時，不會複製使用者介面中現有的主鍵。

 

 



