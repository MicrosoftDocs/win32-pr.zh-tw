---
description: RemoveFolders 動作會移除任何連結至元件的資料夾，這些資料夾已設定為要從來源移除或執行。 只有當這些資料夾是空的時，才會移除這些資料夾。 如果移除資料夾，則會以適當的元件識別碼取消註冊。
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: RemoveFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b476de044ef48b50120575a8d6991d27bf063dec37a026a2f5d2ea0e604abee0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082538"
---
# <a name="removefolders-action"></a>RemoveFolders 動作

RemoveFolders 動作會移除任何連結至元件的資料夾，這些資料夾已設定為要從來源移除或執行。 只有當這些資料夾是空的時，才會移除這些資料夾。 如果移除資料夾，則會以適當的元件識別碼取消註冊。

## <a name="sequence-restrictions"></a>順序限制

RemoveFolders 動作必須在 [RemoveFiles](removefiles-action.md) 動作之後，或可能會從資料夾移除檔案的任何動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述    |
|-------|-------------------------------|
| \[1\] | 已移除資料夾的識別碼。 |



 

## <a name="remarks"></a>備註

安裝程式在卸載應用程式期間，不會自動移除 [CreateFolders 動作](createfolders-action.md) 所建立的資料夾。 您必須將 RemoveFolders 動作撰寫至動作順序，指示安裝程式移除這些資料夾。

若要指定資料夾的名稱和位置，請使用 CreateFolder 資料表的 [目錄] 資料 \_ 行。 [](createfolder-table.md) CreateFolder 資料表中的每個資料夾名稱都假設為定義資料夾位置的屬性。

若要指定擁有資料夾的元件，請使用 [元件資料表](component-table.md)的 [元件] 資料行。

 

 



