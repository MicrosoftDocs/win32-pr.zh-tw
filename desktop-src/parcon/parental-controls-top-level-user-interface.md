---
description: 家長監護 Top-Level 消費者介面
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: 家長監護 Top-Level 消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977946"
---
# <a name="parental-controls-top-level-user-interface"></a>家長監護 Top-Level 消費者介面

系列安全與 Windows 使用者帳戶之間的增強式連結，在 Windows Vista 的取用者導向 Sku 主控台中，會以 **使用者帳戶和家庭安全** 的形式出現在相同的組合類別中。

> [!Note]  
> 當聯結了具有網域加入功能的電腦時，類別目錄會顯示為 **使用者帳戶** 。

 

如果尚未為受控制的使用者設定標準使用者帳戶，主控台中的連結會提供簡單的工作流程，以新增新的 parentally 控制帳戶。

建立帳戶之後，[家長監護] 主控台會為受控制的使用者公開最上層的使用者面向功能。 元素：

-   整體家長監護會控制選項按鈕的限制。
-   獨立活動報告開啟或關閉控制選項按鈕。
-   [設定] 區段中會有條件地顯示 Microsoft 所執行的 Web 限制連結，並顯示可用的核心離線 Microsoft 執行的限制類型。
-   當 Microsoft 或協力廠商註冊消費者介面延伸模組時，會出現 [其他設定] 區域。
-   摘要狀態區域，顯示使用者名稱和磚、[View activity reports] 連結，以及 [家長監護] 設定的狀態。 如果開啟，則顯示會包含 Web 內容篩選器設定層級 (如果 Microsoft 篩選準則為使用中) 或篩選名稱（如果是由協力廠商延伸模組覆寫），以及使用者的離線設定狀態。

整體家長監護 [啟用] 選項按鈕一開始會設定為 [關閉] 狀態。 當系統管理員開啟時，預設也會開啟活動報告，但可能會獨立關閉。 如同家長監護中幾乎所有的設定，設定可能會透過可用的 Api 以程式設計方式執行。

 

 



