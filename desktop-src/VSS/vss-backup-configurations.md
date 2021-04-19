---
description: 有許多支援的備份類型&\# 郵件; 增量、差異和完整&\# 郵件; vss 感知，以及備份設定什麼嗎至 vss。
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: VSS 備份設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967135"
---
# <a name="vss-backup-configurations"></a>VSS 備份設定

有一些可支援的傳統備份類型（累加、差異和完整），也就是 VSS 的認知，以及備份設定什麼嗎至 VSS。

在定義備份設定時，系統要求者和系統的寫入器會指出資料如何寫入儲存裝置、如何部署陰影複製機制，以及需要儲存哪些資訊。 寫入器與要求者之間的互動取決於要求者想要執行的備份類型，以及每個寫入器可支援的 (或架構) 類型：

-   [VSS 備份狀態](vss-backup-state.md)
-   [寫入器備份架構支援](writer-backup-schema-support.md)
-   [檔案層級架構支援](file-level-schema-support.md)

 

 



