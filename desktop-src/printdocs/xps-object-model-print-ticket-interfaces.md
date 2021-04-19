---
description: XPS 檔 API 的這個 IXpsOMPrintTicketResource 介面可讓您存取現有的列印票證，也能在 XPS OM 中建立列印票證。
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: XPS OM 列印票證介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982819"
---
# <a name="xps-om-print-ticket-interfaces"></a>XPS OM 列印票證介面

XPS 檔 API 的這個 [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) 介面可讓您存取現有的列印票證，也能在 xps OM 中建立列印票證。

## <a name="print-ticket-resources"></a>列印票證資源

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)介面可讓程式藉由呼叫支援列印票證之介面的 **GetPrintTicketResource** 方法，來讀取現有列印票證的內容。 藉由呼叫 **SetPrintTicketResource**，可以將新的列印票證資源新增至檔元件。

有三種列印票證層級，可指定列印票證的範圍。 列印票證層級為：工作 (或封裝) 層級、檔層級和頁面層級。 下表顯示列印票證層級、對應的 XPS OM 介面，以及用來存取列印票證資源的方法之間的關聯性。

| 列印票證層級 | 介面                                                | Get 方法                                                                      | Set 方法                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| 工作 (Job)                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| 文件           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| 頁面               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>列印票證內容

您可以從與資源相關聯的資料流程讀取，以存取現有列印票證資源的內容。 [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)介面的 [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream)方法會傳回唯讀資料流程的指標，其中包含列印票證的 XML 格式內容。 列印 [架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)中說明列印票證內容的格式。

您可以建立新的 [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) 介面來建立新的列印票證資源。 有效的 XML 格式列印票證會寫入資料流程，並建立元件 URI 來識別列印票證部分。 如需有效列印票證內容的詳細資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。 資料流程和元件 URI 會以 [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) 呼叫的參數形式傳遞，以設定新的列印票證資源，並藉由呼叫上表中所示的 **SetPrintTicketResource** 方法，將列印票證資源新增至對應的檔部分。

## <a name="print-ticket-inheritance"></a>列印票證繼承

列印票證會繼承具有更大範圍的列印票證屬性。 例如，檔層級列印票證會繼承與檔檔順序相關聯的作業層級列印票證屬性。 同樣地，頁面層級列印票證會繼承與分頁檔相關聯的檔層級列印票證屬性。 在此繼承程式中，較低層級列印票證中指定的屬性會覆寫對應的屬性，這些屬性會繼承自較高層級的列印票證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



