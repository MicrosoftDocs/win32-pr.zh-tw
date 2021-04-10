---
description: 描述 WsdCodeGen 所使用的輸入檔，以及 WsdCodeGen 所產生的輸出檔。
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: 關於 WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026542"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="91269-103">關於 WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="91269-103">About WsdCodeGen</span></span>

<span data-ttu-id="91269-104">WsdCodeGen 會使用 XML 設定檔來判斷服務中繼資料的位置。</span><span class="sxs-lookup"><span data-stu-id="91269-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="91269-105">設定檔也用來定義介面名稱、介面 Guid、類別名稱、方法名稱和其他識別碼。</span><span class="sxs-lookup"><span data-stu-id="91269-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="91269-106">如需此檔案的詳細資訊，請參閱 [WsdCodeGen 設定檔](wsdcodegen-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="91269-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="91269-107">WsdCodeGen 需要兩種類型的輸入檔： XML 設定檔，以及一或多個服務描述檔案 (WSDL 和/或 XSD 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="91269-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="91269-108">WsdCodeGen 會處理這些輸入檔案，並產生兩種類型的輸出檔案：介面檔案和標頭/來源檔案。</span><span class="sxs-lookup"><span data-stu-id="91269-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="91269-109">輸入檔</span><span class="sxs-lookup"><span data-stu-id="91269-109">Input Files</span></span>



| <span data-ttu-id="91269-110">類型</span><span class="sxs-lookup"><span data-stu-id="91269-110">Type</span></span>                      | <span data-ttu-id="91269-111">Description</span><span class="sxs-lookup"><span data-stu-id="91269-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91269-112">組態檔</span><span class="sxs-lookup"><span data-stu-id="91269-112">Configuration file</span></span>        | <span data-ttu-id="91269-113">XML 檔案，表示服務中繼資料的位置，並定義介面名稱、介面 Guid、類別名稱、方法名稱和其他識別碼。</span><span class="sxs-lookup"><span data-stu-id="91269-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="91269-114">服務描述檔案</span><span class="sxs-lookup"><span data-stu-id="91269-114">Service description files</span></span> | <span data-ttu-id="91269-115">描述要在裝置上執行之服務的一或多個 WSDL 或 XSD 檔案。</span><span class="sxs-lookup"><span data-stu-id="91269-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="91269-116">輸出檔</span><span class="sxs-lookup"><span data-stu-id="91269-116">Output Files</span></span>



| <span data-ttu-id="91269-117">類型</span><span class="sxs-lookup"><span data-stu-id="91269-117">Type</span></span>                        | <span data-ttu-id="91269-118">Description</span><span class="sxs-lookup"><span data-stu-id="91269-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91269-119">介面檔</span><span class="sxs-lookup"><span data-stu-id="91269-119">Interface files</span></span>             | <span data-ttu-id="91269-120">IDL (介面定義語言) 檔案，可搭配 MIDL 編譯器使用以產生介面標頭檔。</span><span class="sxs-lookup"><span data-stu-id="91269-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="91269-121">WSDAPI 用戶端和 WSDAPI 服務可以使用此介面檔。</span><span class="sxs-lookup"><span data-stu-id="91269-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="91269-122">C + + 標頭檔和原始檔</span><span class="sxs-lookup"><span data-stu-id="91269-122">C++ header and source files</span></span> | <span data-ttu-id="91269-123">描述訊息合約、命名空間和類型資訊的 c + + 檔案。</span><span class="sxs-lookup"><span data-stu-id="91269-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="91269-124">它們可能包含 proxy 程式碼和/或 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="91269-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="91269-125">Proxy 程式碼會執行服務的介面，並將服務方法呼叫轉譯為發出服務要求的 WSDAPI 作業。</span><span class="sxs-lookup"><span data-stu-id="91269-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="91269-126">Stub 程式碼會將 WSDAPI 服務要求轉譯為呼叫服務方法的程式碼。</span><span class="sxs-lookup"><span data-stu-id="91269-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91269-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="91269-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91269-128">裝置上的 Web 服務程式碼產生器</span><span class="sxs-lookup"><span data-stu-id="91269-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="91269-129">使用 WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="91269-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 



