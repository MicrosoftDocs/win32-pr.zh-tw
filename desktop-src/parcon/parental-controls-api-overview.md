---
description: 家長監護 API 總覽
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: 家長監護 API 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978155"
---
# <a name="parental-controls-api-overview"></a>家長監護 API 總覽

用於家長監護的 Api 會公開原則和內建限制設定，以及記錄功能。

## <a name="settings"></a>設定

提供兩個公用 Api：

-   輕量以 COM 為基礎的最小合規性 API (稱為「合規性 API」，) 主要是讓應用程式判斷是否應該開啟記錄。 此外，還提供簡單的方法：
    -   正在為 web 限制、時間限制、遊戲限制和應用程式限制，取得限制狀態。
    -   正在抓取主動式 Web 內容篩選器的識別碼。
    -   決定是否應該顯示廠商使用者介面專案，與加入網域時的內建隱藏方式一致。
    -   上次為使用者變更設定的時間。
    -   抓取是否需要封鎖使用者的瀏覽器型或類似瀏覽器的檔案下載，以及要求該使用者的 Web 內容篩選器特別允許 URL 的能力。
    -   判斷使用者是否封鎖指定的遊戲。
-   Windows Management Instrumentation (的 WMI) API 存取家長監護命名空間，以完整寫入和讀取所有公開設定的存取權。 家長監護會部署 WMI 提供者，以管理基礎設定存放區的讀取/寫入權限，並適當地強制執行系統管理員和受控制使用者的許可權。

Isv 會要求使用合規性 API，並視需要使用 WMI API，根據應用程式或解決方案的功能來控制適用于子安全性的限制。

## <a name="logging"></a>記錄

-   Windows standard 事件發佈和取用 Api 用於家長監護活動監視。 Windows Vista 附隨報告和追蹤系統改進了先前 Windows (ETW) 功能事件追蹤的效能。 家長監護會在 ETW 中定義其資料的唯一通道。
-   Isv 要求使用事件發佈 API 來記錄使用者活動，如使用家長監護 Api 一節中所指定。

 

 



