---
description: StopServices 動作會停止系統服務。 此動作會查詢 ServiceControl 資料表。
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: StopServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979022"
---
# <a name="stopservices-action"></a>StopServices 動作

StopServices 動作會停止系統服務。 此動作會查詢 [ServiceControl 資料表](servicecontrol-table.md)。

## <a name="sequence-restrictions"></a>順序限制

服務動作必須以下列順序使用：

-   StopServices
-   [DeleteServices](deleteservices-action.md)

下列任一動作：

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 服務顯示名稱。      |
| \[2\] | 服務名稱。              |



 

## <a name="remarks"></a>備註

此動作會要求使用者必須是系統管理員或具有控制服務之許可權的較高許可權，或應用程式屬於受管理安裝的一部分。

 

 



