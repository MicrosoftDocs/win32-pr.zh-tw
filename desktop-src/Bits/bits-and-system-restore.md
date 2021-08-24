---
title: BITS 和系統還原
description: 並非所有 BITS 版本都使用相同的格式來儲存工作。
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702098"
---
# <a name="bits-and-system-restore"></a>BITS 和系統還原

並非所有 BITS 版本都使用相同的格式來儲存工作。 如果您將電腦還原到 BITS 升級之前的還原點，舊版本的 BITS 可能無法讀取目前的作業資訊。 如果發生這種情況，BITS 將刪除工作清單並建立新的空白作業清單。 如此一來，就不會清除與先前的工作清單相關聯的暫存檔案;若要回收磁碟空間，您必須手動刪除檔案。

熟悉 Windows 命令列的使用者可以使用[BITSAdmin 工具](bitsadmin-tool.md)清除 BITS 作業清單，再執行系統還原，以避免這個問題。 若要清除 BITS 作業清單，請執行下列命令：

**bitsadmin/reset/allusers**

請注意，您必須具有系統管理員許可權，才能執行此命令。

 

 




