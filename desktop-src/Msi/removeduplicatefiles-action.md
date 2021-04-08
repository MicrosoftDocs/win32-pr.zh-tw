---
description: RemoveDuplicateFiles 動作會刪除 DuplicateFiles 動作所安裝的檔案。
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: RemoveDuplicateFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690239"
---
# <a name="removeduplicatefiles-action"></a>RemoveDuplicateFiles 動作

RemoveDuplicateFiles 動作會刪除 [DuplicateFiles](duplicatefiles-action.md) 動作所安裝的檔案。

## <a name="sequence-restrictions"></a>順序限制

RemoveDuplicateFiles 動作必須發生在 [InstallValidate](installvalidate-action.md) 動作之後，以及 [InstallFiles](installfiles-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                    |
|-------|-----------------------------------------------|
| \[1\] | 已移除之檔案的識別碼。                   |
| \[9\] | 保存已移除檔案之目錄的識別碼。 |



 

## <a name="remarks"></a>備註

若要使用 RemoveDuplicateFiles 動作刪除以 [DuplicateFiles 動作](duplicatefiles-action.md) 複製的檔案，必須選取與 DuplicateFile 資料表中檔案的專案相關聯的元件才能移除。

使用 [DuplicateFile 資料表](duplicatefile-table.md) 的 DestFolder 資料行來指定屬性名稱，其值可識別目的資料夾。

 

 



