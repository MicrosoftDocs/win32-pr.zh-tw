---
description: WMI 命名空間是一種程式設計物件，可定義一組類別和實例的範圍。 WMI 提供者類別必須定義在命名空間內。
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: 在 WMI 內建立階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192204"
---
# <a name="creating-hierarchies-within-wmi"></a>在 WMI 內建立階層

[*WMI 命名空間*](gloss-n.md) 是一種程式設計物件，可定義一組類別和實例的範圍。 WMI 提供者類別必須定義在命名空間內。

命名空間會描述不同的受控環境，例如 SMS 環境。 由於架構的類別和實例會定義 managed 環境的元件，因此每個新的架構都需要新的命名空間。 例如，根 \\ cimv2 命名空間包含 win32 架構中定義的類別和實例，以及 win32 架構所繼承 (CIM) 類別的父系通用訊息模型。 CIM 類別是由分散式管理工作強制 ([DMTF](https://www.dmtf.org/home)) 所定義。

> [!Note]  
> 若要確保在 WMI 發生失敗並重新啟動時，受管理物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式 (MOF)*](gloss-m.md)檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。

 

WMI 會將命名空間定義為 [**\_ \_ 命名**](--namespace.md)空間系統類別的實例或衍生自 **\_ \_ 命名空間** 的任何類別。 **\_ \_ 命名空間** 系統類別具有名為 **Name** 的單一屬性，這個屬性在父命名空間的範圍內必須是唯一的。 **Name** 屬性也必須包含以字母開頭的字串。 字串中的所有其他字元可以是字母、數位或底線。 所有字元都不區分大小寫。

除了決定子命名空間的唯一名稱之外，父系 WMI 命名空間也可以保護您類別的靜態實例，防止其他提供者意外修改。 例如，您可能會發現將新的命名空間嵌入另一個提供者的現有命名空間，是很方便的。 不過，原始提供者可能會嘗試更新所有類別實例，以符合新的架構。 在這麼做的情況下，原始提供者可能會刪除命名空間中的所有子系子系。 雖然這可能是目標命名空間的適當動作，但它可能會影響子命名空間中不相關的類別實例 (例如，您自己的提供者類別) 。

因此，通常建議您建立命名空間，並將其註冊為與您未直接控制的命名空間不同的命名空間。 如果您的類別只衍生自您公司的一般 CIM 類別或其他類別，則更是如此。 您的命名空間可以在 **根** 命名空間底下，如下所示：

**Root/myCompany/myProduct**

相反地，如果您的新類別衍生自另一個提供者的類別，您可能需要將您的類別儲存在該提供者的子命名空間中。 請注意，這會公開原始提供者意外刪除的新類別。

WMI 提供數種不同的方式來建立命名空間：

-   [使用 MOF 程式碼建立子命名空間](creating-a-child-namespace-with-mof-code.md)
-   [使用 MOF 程式碼建立同級命名空間](creating-a-sibling-namespace-with-mof-code.md)
-   [使用 WMI API 建立命名空間](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



