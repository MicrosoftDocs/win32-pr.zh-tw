---
description: 使用符號連結的程式設計考慮。
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: " (本機檔案系統的程式設計考慮) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981878"
---
# <a name="programming-considerations-local-file-systems"></a> (本機檔案系統的程式設計考慮) 

使用符號連結時，請記住下列程式設計考慮：

-   符號連結可以指向不存在的目標。
-   建立符號連結時，作業系統不會查看目標是否存在。
-   如果應用程式嘗試開啟不存在的目標，則會傳回 **錯誤 \_ \_ \_** 檔案。
-   符號連結是重新分析點。 如需詳細資訊，請參閱 [判斷目錄是否為裝載的資料夾](determining-whether-a-directory-is-a-volume-mount-point.md)。
-   最多可 (63 重新分析點，因此會) 特定路徑中允許的符號連結。

    **Windows Server 2003 和 Windows XP：** 在任何指定的路徑上，都有31個重新分析點的限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>


</dt> <dt>

[永久連結和接合](hard-links-and-junctions.md)
</dt> </dl>

 

 



