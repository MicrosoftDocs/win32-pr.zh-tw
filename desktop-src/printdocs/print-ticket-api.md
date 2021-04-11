---
description: 列印票證 API 可讓應用程式管理和轉換列印票證。
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: 列印票證 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104027694"
---
# <a name="print-ticket-api"></a>列印票證 API

列印票證 API 可讓應用程式管理和轉換列印票證。

列印票證是 XPS 檔元件，其中包含檔中頁面的慣用印表機設定、整份檔，或包含一或多個檔的列印工作。 請注意，列印票證只會在 XPS 檔中找到。

在印表機可以使用列印票證之前，必須先針對印表機的特性（在印表機的列印功能中定義）驗證列印票證。 應用程式會藉由呼叫 Print Ticket API 來執行該驗證。

您可以使用 print [Schema 規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)所定義的列印架構元素來描述 PrintTicket 和 PrintCapabilities。

本主題包含下列 API 元素的相關資訊：

-   [列印票證 API 函式](print-ticket-api-functions.md)
-   [列印票證 API 列舉](print-ticket-api-enumerations.md)

下圖顯示 Print Ticket API 與原生 Windows 應用程式可以使用的其他列印 Api 的關聯性。

![此圖表顯示列印票證 api 與原生 windows 應用程式可以使用的其他列印 api 的關聯性](images/print-apis-pt.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XPS 列印 API](xps-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API](print-spooler-api.md)
</dt> <dt>

[GDI 列印 API](gdi-printing.md)
</dt> <dt>

[列印架構規格](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



