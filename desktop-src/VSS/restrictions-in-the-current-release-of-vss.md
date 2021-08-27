---
description: 針對 Windows Server 2003 版 VSS 所規劃的特定功能並未完全支援：
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Windows Server 2003 中的限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7353b2d52a7222015f051e15ba07830b81d6aedda6323bca4378f459eb602ba8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124508"
---
# <a name="restrictions-in-windows-server-2003"></a>Windows Server 2003 中的限制

針對 Windows Server 2003 版 VSS 所規劃的特定功能並未完全支援：

-   在備份作業期間，只有當只有一個實例有寫入器還原狀態時，才允許指定寫入器類別的多個實例 (請參閱 vss [**\_ WRITERRESTORE \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) ，而非 vss \_ WRE \_ 。 如果符合這個條件，所有寫入器實例都會在備份期間完全參與，產生寫入器元資料檔案，並參與事件處理。
-   在還原作業期間，只有一個寫入器會接收要求者所產生的還原事件。 如果一個以上的寫入器類別實例的寫入器還原狀態設定為非 VSS \_ WRE \_ ，則只會有一個實例接收還原事件。 將接收它們的實例不確定。

 

 



