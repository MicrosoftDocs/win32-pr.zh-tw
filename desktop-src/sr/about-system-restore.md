---
title: 關於系統還原
description: 系統還原會監視系統變更，並將系統狀態儲存為還原點。 如果系統因系統變更而產生系統問題，使用者可以使用還原點中的資料將系統回復為先前的狀態。
ms.assetid: 84fea0f8-22aa-41a9-bb07-e98e9d9b0eee
keywords:
- 系統還原，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5687480b45356fb0be3b586e811c84cfba89ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301539"
---
# <a name="about-system-restore"></a>關於系統還原

系統還原會監視系統變更，並將系統狀態儲存為 *還原點*。 如果系統因系統變更而產生系統問題，使用者可以使用還原點中的資料將系統回復為先前的狀態。

應用程式和系統可在發生系統變更時建立還原點。 您也可以將系統還原設定為定期建立還原點，而且使用者可以隨時建立還原點。 在過去7天內，Windows 7 中的系統還原會每天檢查一次，並建立排定的還原點（如果未在過去7天內建立其他還原點）。 如果過去24小時內未建立任何其他還原點，則 Windows Vista 中的系統還原會建立還原點。 Windows XP 中的系統還原每隔24小時會建立一個檢查點，絕對時間。

系統還原不會還原使用者資料或檔，因此不會導致使用者遺失其檔案、電子郵件、流覽歷程記錄或我的最愛。 Windows 修復環境或安全模式中的使用者也可以使用系統還原，以便在發生問題之前，讓使用者更容易將電腦還原成狀態。

如需詳細資訊，請參閱下列主題：

-   [監視系統](monitoring-the-system.md)
-   [還原系統](restoring-the-system.md)
-   [還原點](restore-points.md)
-   [系統還原 API](system-restore-api.md)

 

 




