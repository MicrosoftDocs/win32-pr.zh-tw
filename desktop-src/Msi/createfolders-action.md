---
description: CreateFolders 動作會針對已設定為要安裝的元件，建立空的資料夾。
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: CreateFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61182143488627c4724e470bf7f5158ed524cb4bc344c972c6744d14f773f6cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105268"
---
# <a name="createfolders-action"></a>CreateFolders 動作

CreateFolders 動作會針對已設定為要安裝的元件，建立空的資料夾。 安裝程式會針對在本機執行並從來源執行的元件建立資料夾。 新建立的資料夾會以適當的元件識別碼進行註冊。

CreateFolders 動作會查詢 [CreateFolder 資料表](createfolder-table.md) 和 [元件資料表](component-table.md)。

## <a name="sequence-restrictions"></a>順序限制

CreateFolders 動作必須在 [InstallFiles](installfiles-action.md) 動作之前，或在將檔案新增至資料夾的任何動作之前執行。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料描述的描述 |
|-------|----------------------------------------|
| \[1\] | 資料夾的目錄識別碼。        |



 

## <a name="remarks"></a>備註

安裝程式不會在應用程式卸載期間自動移除 CreateFolders 動作所建立的資料夾。 只有在動作順序中包含 [RemoveFolders 動作](removefolders-action.md) 時，安裝程式才會移除資料夾。

 

 



