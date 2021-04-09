---
title: 適用于開發人員的工作排程器
description: 此工作排程器可讓您在選擇的電腦上自動執行例行工作。 工作排程器藉由監視您所選擇的任何準則 (稱為「觸發程式」) 然後在符合這些準則時執行這些工作。
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- 適用于開發人員的工作排程器
- 適用于開發的工作排程器
- 使用工作排程器開發
- 工作排程器，入口網站頁面
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2019
ms.locfileid: "104092325"
---
# <a name="task-scheduler-for-developers"></a>適用于開發人員的工作排程器

> [!IMPORTANT]
> 本主題和本節中的其他主題適用于開發人員物件。 如果您想要以系統管理員或 IT 專業人員的容量使用工作排程器元件，請參閱 [工作排程器](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler)。

## <a name="about-the-task-scheduler"></a>關於工作排程器

此工作排程器可讓您在選擇的電腦上自動執行例行工作。 工作排程器藉由監視您所選擇的任何準則 (稱為「觸發程式」) 然後在符合這些準則時執行這些工作。

您可以使用工作排程器來執行工作，例如啟動應用程式、傳送電子郵件訊息，或顯示訊息方塊。 您可以排程工作來執行，以回應這些事件或觸發程式。 

- 當發生特定的系統事件時。
- 在特定時間。
- 在每日排程的特定時間。
- 在每週排程的特定時間。
- 每月排程的特定時間。
- 在每一周的特定時間排程。
- 當電腦進入閒置狀態時。
- 當工作已註冊時。
- 系統啟動時。
- 當使用者登入時。
- 當終端機伺服器會話變更狀態時。

## <a name="developers"></a>開發人員

工作排程器提供這些形式的 Api。

- 工作排程器2.0：針對 c + + 和腳本開發分別提供介面和物件。
- 工作排程器1.0：提供 c + + 開發的介面。

## <a name="run-time-requirements"></a>執行階段需求求

工作排程器需要下列作業系統。

- 工作排程器2.0：用戶端需要 Windows Vista 或更新版本。 伺服器需要 Windows Server 2008 或更新版本。
- 工作排程器1.0：用戶端需要 Windows Vista 或 Windows XP。 伺服器需要 Windows Server 2008 或 Windows Server 2003。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [工作排程器的新功能](what-s-new-in-task-scheduler.md) | 工作排程器所引進之新功能的摘要。 |
| [關於工作排程器](about-the-task-scheduler.md) | 工作排程器 API 的一般概念資訊。 |
| [使用工作排程器](using-the-task-scheduler.md) | 示範如何使用工作排程器 Api 的程式碼範例。 |
| [工作排程器參考](task-scheduler-reference.md) | 工作排程器 Api 和工作排程器架構的詳細參考資訊。 |