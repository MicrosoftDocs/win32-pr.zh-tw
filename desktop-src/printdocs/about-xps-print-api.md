---
description: XPS&\# 160;列印&\# 160;API 提供了列印多工緩衝處理器的介面，可讓應用程式用來列印將 XPS 檔傳送至印表機的作業。
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: 關於 XPS 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950858"
---
# <a name="about-the-xps-print-api"></a>關於 XPS 列印 API

[XPS 列印 API](xps-printing.md)提供了列印多工緩衝處理器的介面，可讓應用程式用來列印將 XPS 檔傳送至印表機的作業。

如果目的地印表機使用 XPSDrv 印表機驅動程式，則「XPS 列印」 API 可讓 XPSDrv 印表機驅動程式在列印多工緩衝處理器處理列印工作時接收檔事件。 如需傳送至 XPSDrv 印表機驅動程式的檔事件描述，請參閱 [XPS 驅動程式檔事件](/windows-hardware/drivers/print/xps-driver-document-events)。

如果目的地印表機使用 GDI 印表機驅動程式，則 [Xps 列印 API](xps-printing.md) 可讓系統處理將列印工作資料從 XPS 格式轉換成增強型中繼檔的必要轉換， (EMF) 格式，也就是 GDI 印表機驅動程式所使用的格式。 如需 GDI 印表機驅動程式檔事件的說明，請參閱 [DocumentEvent 函數](documentevent.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 XPS 列印 API](using-the-xps-print-api.md)
</dt> <dt>

[XPS 列印 API 參考](xpsprint-api.md)
</dt> </dl>

 

 
