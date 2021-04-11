---
description: DeleteServices 動作會停止服務，並從系統中移除其註冊。 此動作會查詢 ServiceControl 資料表。
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: DeleteServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319515"
---
# <a name="deleteservices-action"></a>DeleteServices 動作

DeleteServices 動作會停止服務，並從系統中移除其註冊。 此動作會查詢 [ServiceControl 資料表](servicecontrol-table.md)。

## <a name="sequence-restrictions"></a>順序限制

服務動作必須以下列順序使用：

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。
4.  [InstallServices 動作](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 服務顯示名稱。      |
| \[2\] | 服務名稱。              |



 

## <a name="remarks"></a>備註

這項動作需要使用者是系統管理員，或具有可刪除服務或應用程式屬於受管理安裝之許可權的更高許可權。

 

 



