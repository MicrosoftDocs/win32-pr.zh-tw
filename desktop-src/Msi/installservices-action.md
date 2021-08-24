---
description: InstallServices 動作會為系統註冊服務。 此動作會查詢 ServiceInstall 資料表。
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: InstallServices 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787018"
---
# <a name="installservices-action"></a>InstallServices 動作

InstallServices 動作會為系統註冊服務。 此動作會查詢 [ServiceInstall 資料表](serviceinstall-table.md)。

## <a name="sequence-restrictions"></a>順序限制

服務動作必須以下列順序使用。

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

下列任何一個動作： [InstallFiles](installfiles-action.md)、 [RemoveFiles](removefiles-action.md)、 [DuplicateFiles](duplicatefiles-action.md)、 [MoveFiles](movefiles-action.md)、 [PatchFiles](patchfiles-action.md)和 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作。

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

此動作會要求使用者必須是系統管理員，或擁有具有安裝服務或應用程式屬於受管理安裝之許可權的更高許可權。

 

 



