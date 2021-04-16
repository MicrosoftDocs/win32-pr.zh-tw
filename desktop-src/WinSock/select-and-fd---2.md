---
description: 因為通訊端不是以 UNIX 樣式、小型、非負整數表示，所以在 Windows 通訊端中，select 函式的實作為變更。
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Select、FD_SET 和 FD_XXX 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513080"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Select、FD \_ SET 和 FD \_ XXX 宏

因為通訊端不是以 UNIX 樣式、小型、非負整數表示，所以在 Windows 通訊端中， [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式的實作為變更。 每一組通訊端仍會以 **FD \_ set** 結構表示，但不會儲存為位元遮罩，而是會實作為通訊端陣列。 為了避免潛在的問題，應用程式必須遵守 FD XXX 宏的使用， \_ 以設定、初始化、清除和檢查 [**fd \_ 設定**](/windows/desktop/api/winsock/nf-winsock-fd_set) 結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 



