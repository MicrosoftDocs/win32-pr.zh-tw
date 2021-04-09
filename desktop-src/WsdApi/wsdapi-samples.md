---
description: Windows Server 2008 的 Windows SDK 隨附兩個 WSDAPI 範例。
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: WSDAPI 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692156"
---
# <a name="wsdapi-samples"></a>WSDAPI 範例

Windows Server 2008 的 Windows SDK 隨附兩個 WSDAPI 範例。 您可以在 <Windows SDK Install Folder> \\ 範例 \\ Web WSDAPI 中找到範例的原始程式碼 \\ 。 您可以從 [下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)取得此版本的 SDK。 Windows Vista SDK 無法使用這些範例。

股票報價範例 (位於 <Windows SDK Install Folder> \\ 範例 \\ Web \\ WSDAPI \\ StockQuote) 示範具有基本訊息功能的服務。 檔案服務範例 (位於 <Windows SDK Install Folder> \\ 範例 \\ Web \\ WSDAPI \\ FileService) 示範具有 advanced 功能的服務，例如非同步通訊、附件和事件。

這兩個範例都包含下列檔案類型。

-   包含服務描述的 WSDL 檔案。
-   用來產生 WSDAPI 程式碼的[WsdCodeGen 設定檔](wsdcodegen-configuration-file.md)。
-   產生的 c + + 標頭檔和原始檔。
-   用戶端和服務執行檔案。
-   Visual Studio 專案和方案檔。

這兩個範例都會 ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)) 、裝置 Proxy ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) 和服務 proxy ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)) 來執行裝置主機。 此外，檔案服務範例會示範如何使用非同步訊息 ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback)、 [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)) 、附件 ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment)、 [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) 和事件。

範例中所含的 FileServiceContract. vcproj 和 StockQuoteContract. vcproj 檔案會呼叫 [WsdCodeGen](web-services-for-devices-code-generator.md) ，以從 WsdCodeGen 設定檔中指定的 WSDL 檔案產生 c + + 標頭和來源檔案。 這表示，如果已變更範例 WSDL 或 WsdCodeGen 設定檔，並重建範例專案，WsdCodeGen 會自動產生新的標頭和原始程式檔，以反映變更。 這是建立 WSDAPI 應用程式的慣用方法。 通常會從命令列呼叫 WsdCodeGen。 開啟相關的 \* vcproj 檔案，以查看範例 WsdCodeGen 命令列呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 上的 WSD 應用程式開發](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



