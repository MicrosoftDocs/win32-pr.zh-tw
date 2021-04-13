---
title: 工作註冊資訊
description: 註冊資訊可讓您以數種不同的方式來識別工作。 例如，作者可以識別工作、撰寫工作的方式 (稱為工作來源) 和註冊日期。
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- 註冊資訊工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300032"
---
# <a name="task-registration-information"></a>工作註冊資訊

註冊資訊可讓您以數種不同的方式來識別工作。 例如，作者可以識別工作、撰寫工作的方式 (稱為工作來源) 和註冊日期。

## <a name="using-registration-information"></a>使用註冊資訊

註冊資訊通常會在工作建立時指定，然後以下列方式使用：

-   由工作排程器使用者介面顯示。
-   取得或設定 c + + 應用程式或腳本。
-   在企業環境中，當列舉所有已註冊的工作時，用來做為搜尋準則。

## <a name="types-of-registration-information"></a>註冊資訊的類型

工作註冊資訊是由 [**RegistrationInfo**](registrationinfo.md) 物件的屬性所定義，用於腳本應用程式、c + + 應用程式的 [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) 介面屬性，以及 [**RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) 專案的子項目，以讀取或寫入 XML。

這些屬性可讓您存取下列類型的註冊資訊：

-   工作作者

    工作排程器設定工作建立時的作者。

-   工作註冊日期

    工作排程器在工作註冊時設定此日期。

-   工作描述

    使用者定義的描述，其中可能包含用來啟動工作的觸發程式，或工作執行的動作。

-   工作檔

    工作所需的使用者提供檔。

-   工作安全描述項

    使用者提供的安全描述項。

-   工作來源

    描述工作來源的使用者提供資訊。 例如，工作可能源自元件、服務、應用程式或使用者。

-   工作 URI

    工作 (URI) 的統一資源識別項。

-   工作版本

    當有多個工作版本存在時所使用的使用者提供資訊。

-   XML 文字

    XML 格式的註冊資訊版本。 請注意，您可以直接透過這個 XML 來設定或修改註冊資訊，適當的物件和介面屬性也會隨之更新。

## <a name="registering-tasks"></a>註冊工作

工作可以在建立工作定義之後註冊，而且註冊資訊和設定值是由使用者提供。 使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法來註冊工作，以編寫應用程式的腳本，或使用 [**ITaskFolder：： RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法來進行 c + + 應用程式。 如果您想要使用 XML 來定義工作，請使用 [**TaskFolder. RegisterTask**](taskfolder-registertask.md) 方法來編寫應用程式的腳本，並使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 方法來進行 c + + 應用程式。

在上面所述的方法中，您可以指定要執行工作的安全性內容。 您必須是系統管理員，才能將工作排程在非您自己的內容下執行。 如需有關執行工作之安全性內容的詳細資訊，請參閱執行工作的 [安全性](security-contexts-for-running-tasks.md)內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 




