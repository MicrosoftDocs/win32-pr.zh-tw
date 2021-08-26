---
description: ModuleSignature 資料表包含識別合併模組所需的所有資訊。
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: 撰寫 ModuleSignature 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c7aaa84b7e5f2db2327bbb272d195333b7a82e609a2dfe2dc72b82eaad9bd09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045408"
---
# <a name="authoring-modulesignature-tables"></a>撰寫 ModuleSignature 資料表

[ModuleSignature 資料表](modulesignature-table.md)包含識別合併模組所需的所有資訊。

ModuleID 欄位是此資料表的主鍵，而且必須遵循在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的慣例。 例如，如果 merge 模組的可讀取名稱是 MyLibrary，而 merge 模組的 GUID 是 {880DE2F0-CDD8-11D1-A849-006097ABDE17}，則 ModuleSignature 資料表之 ModuleID 資料行中的專案會變成 MyLibrary 880DE2F0 CDD8 11D1 A849 \_ \_ \_ \_ 。

在 [ModuleSignature] 資料表的 [語言] 欄位中，輸入合併模組之預設語言的小數識別碼。

在 [版本] 欄位中輸入合併模組的版本。

 

 



