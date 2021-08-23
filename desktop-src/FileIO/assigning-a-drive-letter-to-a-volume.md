---
description: 如果沒有已指派給該磁碟機號的磁片區，您可以使用 SetVolumeMountPoint 函式，將磁碟機號 (例如 X：指派給 \) 本機磁片區。
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: 指派磁碟機號給磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766220"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>指派磁碟機號給磁片區

如果沒有 \) 已指派給該磁碟機號的磁片區，您可以使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將磁碟機號 (例如 X：指派給本機磁片區。 如果本機磁片區已經有磁碟機號。 然後 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 將會失敗。 若要處理這種情況，請先使用 [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) 函式刪除磁碟機號。 如需範例程式碼，請參閱 [編輯磁碟機號指派](editing-drive-letter-assignments.md)。

系統最多可為每個磁片區支援一個磁碟機號。 因此，您不能有 C： \\ 和 F： \\ 代表相同的磁片區。

> [!Caution]
>
> 刪除現有的磁碟機號並指派新的磁碟機號，可能會中斷現有的路徑，例如桌面快捷方式中的路徑。 它也可能會中斷變更磁碟機號的程式路徑。 使用 Windows 的虛擬記憶體管理時，這可能會中斷應用程式，讓系統處於不穩定且可能無法使用的狀態。 程式設計人員必須負責避免這類潛在的最受到自然災害。

 

 

 



