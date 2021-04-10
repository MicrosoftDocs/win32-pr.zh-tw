---
title: WsUtil 編譯器工具
description: WsUtil.exe 的 Windows Web 服務編譯器工具支援服務模型和資料類型的序列化。 它會處理 WSDL、XML 架構和原則檔，並產生 C 標頭和原始程式檔。
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- 適用于 Windows 的 WsUtil 編譯器工具 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933733"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="265b0-107">WsUtil 編譯器工具</span><span class="sxs-lookup"><span data-stu-id="265b0-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="265b0-108">WsUtil.exe 的 Windows Web 服務編譯器工具支援 [服務模型](service-model-layer-overview.md) 和資料類型的 [序列化](serialization.md) 。</span><span class="sxs-lookup"><span data-stu-id="265b0-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="265b0-109">它會處理 WSDL、XML 架構和原則檔，並產生 C 標頭和原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="265b0-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="265b0-110">這項工具與適用于 managed 程式碼的 WSDL 編譯器工具類似，但其目的是改為原生程式碼。</span><span class="sxs-lookup"><span data-stu-id="265b0-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="265b0-111">為了支援 [服務模型](service-model-layer-overview.md)，WsUtil.exe 會產生用於用戶端和服務的標頭。</span><span class="sxs-lookup"><span data-stu-id="265b0-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="265b0-112">它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。</span><span class="sxs-lookup"><span data-stu-id="265b0-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="265b0-113">為了支援 [序列化](serialization.md)，編譯器會針對全域專案定義產生專案描述的標頭，以及序列化引擎所取用之 proxy 檔案中的所有類型定義資訊。</span><span class="sxs-lookup"><span data-stu-id="265b0-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="265b0-114">如需處理 WSDL 檔案、XML 架構檔案和 web 服務原則檔案的命令列選項，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="265b0-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="265b0-115">Web 服務編譯器工具</span><span class="sxs-lookup"><span data-stu-id="265b0-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="265b0-116">WSDL 和服務合約</span><span class="sxs-lookup"><span data-stu-id="265b0-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="265b0-117">結構描述支援</span><span class="sxs-lookup"><span data-stu-id="265b0-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="265b0-118">原則支援</span><span class="sxs-lookup"><span data-stu-id="265b0-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="265b0-119">安全性</span><span class="sxs-lookup"><span data-stu-id="265b0-119">Security</span></span>

<span data-ttu-id="265b0-120">當您使用 WsUtil 時，請注意下列問題，並觀察適當的預防措施：</span><span class="sxs-lookup"><span data-stu-id="265b0-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="265b0-121">Wsutil 不會透過網路抓取 XML 中繼資料，而且 Wsutil 無法解析輸入中繼資料檔案中的 import 和/或 include 語句。</span><span class="sxs-lookup"><span data-stu-id="265b0-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="265b0-122">Wsutil 會開啟並讀取 wsdl、xsd 和原則檔。</span><span class="sxs-lookup"><span data-stu-id="265b0-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="265b0-123">XML 中繼資料不會受到防篡改。</span><span class="sxs-lookup"><span data-stu-id="265b0-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="265b0-124">請確定您只使用 wsdl、xsd 和原則檔案是從受信任的來源取得，並且確定在使用檔案之前和之後都不會受到篡改的保護。</span><span class="sxs-lookup"><span data-stu-id="265b0-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="265b0-125">仔細檢查輸入檔的內容，並驗證檔案的內容可安全地在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="265b0-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="265b0-126">Wsutil.exe 不會針對中繼資料檔案的真實性進行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="265b0-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="265b0-127">Wsutil 會產生標頭和存根檔案，這些檔案不會受到防篡改。</span><span class="sxs-lookup"><span data-stu-id="265b0-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="265b0-128">您必須在 wsutil.exe 所產生的原始程式檔上設定正確的層級存取權限，以防止 unauthoritized 存取這些檔案。</span><span class="sxs-lookup"><span data-stu-id="265b0-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="265b0-129">Wsutil 會使用 StreamWriter 來建立輸出檔。</span><span class="sxs-lookup"><span data-stu-id="265b0-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="265b0-130">使用者必須留意到 Wsutil 可以覆寫本機檔案，而且使用/out 參數指定輸出檔的安全檔案名和目錄時，也應該小心。</span><span class="sxs-lookup"><span data-stu-id="265b0-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="265b0-131">在 wsutil.exe 中載入的 Wsutil 或 wsutilhelper.dll，可能會在攻擊或處理非常大量的輸入中繼資料時，非預期地終止或耗用大量的系統資源。</span><span class="sxs-lookup"><span data-stu-id="265b0-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="265b0-132">此工具是設計用來在開發期間使用，只應使用此工具作為開發時間工具。</span><span class="sxs-lookup"><span data-stu-id="265b0-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="265b0-133">在仲介層中使用可能無法安全地處理原則資訊。</span><span class="sxs-lookup"><span data-stu-id="265b0-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="265b0-134">Wsutilhelper.dll helper DLL 會載入至 managed wsutil.exe 來處理原則資訊。</span><span class="sxs-lookup"><span data-stu-id="265b0-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="265b0-135">使用者應確定二進位路徑中不存在具有相同檔案名的惡意二進位檔。</span><span class="sxs-lookup"><span data-stu-id="265b0-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="265b0-136">同樣地，使用者應確定在組建環境中，已正確設定二進位路徑，且不存在具有相同 "wsutil.exe" 名稱的惡意二進位檔。</span><span class="sxs-lookup"><span data-stu-id="265b0-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="265b0-137">如果可能的話，Wsutil 會為作業和結構欄位產生 SAL 注釋。</span><span class="sxs-lookup"><span data-stu-id="265b0-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="265b0-138">Wsutil 產生之檔案的使用者應遵循透過 SAL 注釋指定的需求。</span><span class="sxs-lookup"><span data-stu-id="265b0-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="265b0-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="265b0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265b0-140">服務模型層總覽</span><span class="sxs-lookup"><span data-stu-id="265b0-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="265b0-141">序列 化</span><span class="sxs-lookup"><span data-stu-id="265b0-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="265b0-142">Web 服務編譯器工具</span><span class="sxs-lookup"><span data-stu-id="265b0-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="265b0-143">WSDL 支援</span><span class="sxs-lookup"><span data-stu-id="265b0-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="265b0-144">結構描述支援</span><span class="sxs-lookup"><span data-stu-id="265b0-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="265b0-145">原則支援</span><span class="sxs-lookup"><span data-stu-id="265b0-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 




