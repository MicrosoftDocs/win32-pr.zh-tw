---
title: 關於工作排程器
description: 工作排程器服務可讓您在所選電腦上執行自動化工作。
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- 工作排程器工作排程器，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca865fe98ffb56f2bb6e9310e31d38bdaa804a63da07e486bbc89a0cd9ebcdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072708"
---
# <a name="about-the-task-scheduler"></a>關於工作排程器

工作排程器服務可讓您在所選電腦上執行自動化工作。 使用此服務時，您可以將任何程式排程在方便的時間執行，或是在發生特定事件時執行。 工作排程器會監視您所選擇的時間或事件準則，然後在符合這些準則時執行工作。

## <a name="where-task-scheduler-is-installed"></a>安裝工作排程器的位置

系統會自動安裝數個 Microsoft 作業系統的工作排程器。

工作排程器1.0 與 Windows Server 2003、Windows XP 和 Windows 2000 作業系統一起安裝。

工作排程器2.0 與 Windows Vista 和 Windows Server 2008 一起安裝。

工作排程器 2.0 API 應該用於開發在 Windows Vista 上使用工作排程器服務的應用程式。 如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md)。

每次啟動作業系統時，就會啟動工作排程器。 您可以透過工作排程器的圖形化使用者介面 (GUI) 或透過此 SDK 中所述的工作排程器 API 來執行它。

## <a name="information-about-tasks"></a>工作的相關資訊

工作是工作排程器的主要元件。 如需哪些工作及其元件的相關資訊，請參閱下列主題：

-   [工作](tasks.md)
-   [工作動作](task-actions.md)
-   [工作觸發程式](task-triggers.md)
-   [工作註冊資訊](task-registration-information.md)
-   [工作閒置條件](task-idle-conditions.md)
-   [工作的安全性內容](security-contexts-for-running-tasks.md)
-   [重複工作](repeating-a-task.md)
-   [自動維護](task-maintenence.md)

如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 




