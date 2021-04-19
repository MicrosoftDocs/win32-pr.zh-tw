---
description: 您可以在 Microsoft .NET Framework 3.0 和更新版本的 Microsoft .NET Framework，以及 Windows Vista 和更新版本的 Windows 中使用列印架構和相關技術。
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: 列印架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106993792"
---
# <a name="print-schema"></a>列印架構

您可以在 Microsoft .NET Framework 3.0 和更新版本的 Microsoft .NET Framework，以及 Windows Vista 和更新版本的 Windows 中使用列印架構和相關技術。 XPS 檔和 XPS 物件模型可以使用列印 [架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)中描述的列印票證物件，指定檔對印表機和觀看應用程式的列印喜好設定。

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)是可下載的檔，其中包含列印架構的相關資訊，以及如何在檔和列印中使用它。 在線上提供的資訊僅供參考，網址為： [舊版列印架構參考](print-schema.md);但是，它可能不會正確地反映出目前版本的 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。 如需最新的設計資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) 。

## <a name="print-schema-overview"></a>列印架構總覽

列印架構是一種階層式結構化的 XML 架構，用來組織和描述印表機或列印工作的屬性。 列印架構包含兩個元件： Print Schema 關鍵字和 Print Schema Framework。 列印架構關鍵字是一組描述印表機屬性和列印工作格式化意圖的元素實例。 Print Schema Framework 會定義 XML 專案型別的階層式結構化集合，以及如何搭配使用這些專案類型。

稱為 *PrintCapabilities* 和 *PrintTicket* 的列印架構技術，是使用 print schema Framework 所指定的 print schema 關鍵字來建立。 列印架構規格支援協力廠商的架構延伸，讓列印架構使用者不受限於列印架構關鍵字所定義的屬性、功能、選項或 ParameterInit 實例。 協力廠商元素實例可以加入至由 Print Schema 關鍵字定義的元素實例;不過，私用的協力廠商屬性實例必須屬於與建立命名空間的協力廠商清楚相關聯的命名空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[舊版列印架構參考](print-schema.md)
</dt> <dt>

[雙向列印機通訊 (硬體開發人員中心) ](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
