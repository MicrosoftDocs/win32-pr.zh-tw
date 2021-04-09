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
# <a name="wsdapi-samples"></a><span data-ttu-id="7f715-103">WSDAPI 範例</span><span class="sxs-lookup"><span data-stu-id="7f715-103">WSDAPI Samples</span></span>

<span data-ttu-id="7f715-104">Windows Server 2008 的 Windows SDK 隨附兩個 WSDAPI 範例。</span><span class="sxs-lookup"><span data-stu-id="7f715-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="7f715-105">您可以在 <Windows SDK Install Folder> \\ 範例 \\ Web WSDAPI 中找到範例的原始程式碼 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7f715-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="7f715-106">您可以從 [下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)取得此版本的 SDK。</span><span class="sxs-lookup"><span data-stu-id="7f715-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="7f715-107">Windows Vista SDK 無法使用這些範例。</span><span class="sxs-lookup"><span data-stu-id="7f715-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="7f715-108">股票報價範例 (位於 <Windows SDK Install Folder> \\ 範例 \\ Web \\ WSDAPI \\ StockQuote) 示範具有基本訊息功能的服務。</span><span class="sxs-lookup"><span data-stu-id="7f715-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="7f715-109">檔案服務範例 (位於 <Windows SDK Install Folder> \\ 範例 \\ Web \\ WSDAPI \\ FileService) 示範具有 advanced 功能的服務，例如非同步通訊、附件和事件。</span><span class="sxs-lookup"><span data-stu-id="7f715-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="7f715-110">這兩個範例都包含下列檔案類型。</span><span class="sxs-lookup"><span data-stu-id="7f715-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="7f715-111">包含服務描述的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="7f715-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="7f715-112">用來產生 WSDAPI 程式碼的[WsdCodeGen 設定檔](wsdcodegen-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="7f715-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="7f715-113">產生的 c + + 標頭檔和原始檔。</span><span class="sxs-lookup"><span data-stu-id="7f715-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="7f715-114">用戶端和服務執行檔案。</span><span class="sxs-lookup"><span data-stu-id="7f715-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="7f715-115">Visual Studio 專案和方案檔。</span><span class="sxs-lookup"><span data-stu-id="7f715-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="7f715-116">這兩個範例都會 ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)) 、裝置 Proxy ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) 和服務 proxy ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)) 來執行裝置主機。</span><span class="sxs-lookup"><span data-stu-id="7f715-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="7f715-117">此外，檔案服務範例會示範如何使用非同步訊息 ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback)、 [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)) 、附件 ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment)、 [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) 和事件。</span><span class="sxs-lookup"><span data-stu-id="7f715-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="7f715-118">範例中所含的 FileServiceContract. vcproj 和 StockQuoteContract. vcproj 檔案會呼叫 [WsdCodeGen](web-services-for-devices-code-generator.md) ，以從 WsdCodeGen 設定檔中指定的 WSDL 檔案產生 c + + 標頭和來源檔案。</span><span class="sxs-lookup"><span data-stu-id="7f715-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="7f715-119">這表示，如果已變更範例 WSDL 或 WsdCodeGen 設定檔，並重建範例專案，WsdCodeGen 會自動產生新的標頭和原始程式檔，以反映變更。</span><span class="sxs-lookup"><span data-stu-id="7f715-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="7f715-120">這是建立 WSDAPI 應用程式的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="7f715-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="7f715-121">通常會從命令列呼叫 WsdCodeGen。</span><span class="sxs-lookup"><span data-stu-id="7f715-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="7f715-122">開啟相關的 \* vcproj 檔案，以查看範例 WsdCodeGen 命令列呼叫。</span><span class="sxs-lookup"><span data-stu-id="7f715-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f715-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f715-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f715-124">Windows 上的 WSD 應用程式開發</span><span class="sxs-lookup"><span data-stu-id="7f715-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



