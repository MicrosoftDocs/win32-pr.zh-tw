---
description: WMI 支援不同的執行緒模型，取決於提供者的裝載方式和提供者功能的類型，例如類別或屬性。
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: 選擇正確的註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a252e9013e828f5dc2c6e4c7228919d0834d0edb3da5f699cbe0306a38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131800"
---
# <a name="choosing-correct-registration"></a>選擇正確的註冊

WMI 支援不同的執行緒模型，取決於提供者的裝載方式和提供者功能的類型，例如 [類別](writing-a-class-provider.md) 或 [屬性](writing-a-property-provider.md)。 例如，低 [*耦合提供者*](gloss-d.md) 不支援所有類型的提供者功能。 如需不同裝載模型及其設定方式的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

## <a name="in-process-providers"></a>In-Process 提供者

同進程提供者是在共用的主機進程中執行，Wmiprvse.exe。 大部分的內建提供者類型都會使用多執行緒的單元 (MTA) 模型。

MTA 模型支援下列類型的提供者功能：

-   [類別提供者](writing-a-class-provider.md)
-   [執行個體提供者](writing-an-instance-provider.md)
-   [方法提供者](writing-a-method-provider.md)
-   [屬性提供者](writing-a-property-provider.md)
-   [事件提供者](writing-an-event-provider.md)
-   [事件取用者提供者](writing-an-event-consumer-provider.md)

針對某些類型的提供者功能，支援單一執行緒的單元 (STA) 模型：

-   [執行個體提供者](writing-an-instance-provider.md)
-   [方法提供者](writing-a-method-provider.md)
-   [事件提供者](writing-an-event-provider.md)
-   [事件取用者提供者](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>跨進程提供者

裝載于不同共用服務主機的提供者支援下列提供者功能：

-   [類別提供者](writing-a-class-provider.md)
-   [執行個體提供者](writing-an-instance-provider.md)
-   [方法提供者](writing-a-method-provider.md)
-   [屬性提供者](writing-a-property-provider.md)
-   [事件提供者](writing-an-event-provider.md)
-   [事件取用者提供者](writing-an-event-consumer-provider.md)

如需共用服務主機的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

## <a name="decoupled-providers"></a>低耦合提供者

低耦合提供者是裝載在應用程式中。 如需詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。 在 .NET Framework 中使用 WMI 建立的提供者會分離。 低耦合提供者支援下列提供者功能：

-   [執行個體提供者](writing-an-instance-provider.md)
-   [方法提供者](writing-a-method-provider.md)
-   [事件提供者](writing-an-event-provider.md)
-   [事件取用者提供者](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[提供者裝載和安全性](provider-hosting-and-security.md)
</dt> </dl>

 

 



