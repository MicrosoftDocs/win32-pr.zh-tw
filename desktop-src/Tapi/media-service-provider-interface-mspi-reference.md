---
description: 本檔概述的介面提供了可讓 MSP 與 Microsoft 電話語音環境互動的方法，並可讓 TAPI 3 應用程式使用 Msp 媒體控制項。
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: 媒體服務提供者介面 (MSPI) 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981742"
---
# <a name="media-service-provider-interface-mspi-reference"></a>媒體服務提供者介面 (MSPI) 參考

本檔概述的介面提供了可讓 MSP 與 Microsoft 電話語音環境互動的方法，並可讓 TAPI 3 應用程式使用 MSP 的媒體控制項。



| 媒體服務提供者介面介面      | Description                                                                                                                                                                            | 必要？ |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | 僅公開至 TAPI。 TAPI DLL 的主要 MSP 介面。 TAPI 3 呼叫此介面上的 **CoCreateInstance** 來建立 MSP 物件。                                               | Yes       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | 公開給應用程式。 提供的方法可讓應用程式抓取資料流程上的資訊、啟動、暫停或停止資料流程，以及選取或取消選取資料流程上的終端機。 | Yes       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | 公開給應用程式。 提供可讓應用程式建立或移除資料流程的方法。                                                                                       | Yes       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | 公開給應用程式。 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)的列舉值介面。                                                                                                        | Yes       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | 公開給應用程式。 提供的方法可讓應用程式抓取子串流上的資訊、啟動、暫停或停止子串流，以及選取或取消選取終端。          | 選擇性  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | 公開給應用程式。 提供可讓應用程式建立或移除子串流的方法。                                                                                    | 選擇性  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | 公開給應用程式。 [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)的列舉值介面。                                                                                                  | 選擇性  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | 公開給應用程式。 取得 [終端機物件](terminal-object.md)的資訊，例如支援的終端電話和媒體。                                                    | Yes       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | 公開給應用程式。 提供方法來查詢可用的終端機，並建立額外的終端機。                                                                             | Yes       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | 公開給應用程式。 抓取可插入的終端機類別和超類的相關資訊;衍生自 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 介面。           | Yes       |



 

## <a name="media-service-provider-interface-types"></a>媒體服務提供者介面類別型

-   [**MSP \_ 位址 \_ 事件**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**MSP \_ 通話 \_ 事件**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**MSP \_ 事件**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**MSP \_ 事件 \_ 資訊**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體服務提供者介面 (MSPI) ](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
