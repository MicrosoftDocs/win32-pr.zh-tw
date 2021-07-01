---
description: 本節說明 Microsoft Windows 所支援的檔技術。
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS 文件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119983"
---
# <a name="xps-documents"></a><span data-ttu-id="526c8-103">XPS 文件</span><span class="sxs-lookup"><span data-stu-id="526c8-103">XPS Documents</span></span>

<span data-ttu-id="526c8-104">本節說明 Microsoft Windows 所支援的檔技術。</span><span class="sxs-lookup"><span data-stu-id="526c8-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="526c8-105">選擇檔技術</span><span class="sxs-lookup"><span data-stu-id="526c8-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="526c8-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="526c8-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="526c8-107">XPS 檔工具</span><span class="sxs-lookup"><span data-stu-id="526c8-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="526c8-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="526c8-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="526c8-109">選擇檔技術</span><span class="sxs-lookup"><span data-stu-id="526c8-109">Choosing a Document Technology</span></span>

<span data-ttu-id="526c8-110">Microsoft 提供數種不同的檔技術來支援各種不同的檔應用程式：</span><span class="sxs-lookup"><span data-stu-id="526c8-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="526c8-111">**XPS 和 OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="526c8-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="526c8-112">在 Windows 8 和更新版本的 Windows 中，可支援 XPS 和 OpenXPS。</span><span class="sxs-lookup"><span data-stu-id="526c8-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="526c8-113">請參閱上圖，以判斷 XPS 和 OpenXPS 的正確使用案例。</span><span class="sxs-lookup"><span data-stu-id="526c8-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="526c8-114">如需有關這些檔技術的詳細資訊，請參閱 [Open XML 檔規格 (OpenXPS) ](https://www.ecma-international.org/publications/standards/Ecma-388.htm)。</span><span class="sxs-lookup"><span data-stu-id="526c8-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="526c8-115">在搭配 Windows 8 和 Windows Server 2012 使用 OpenXPS 的情況下，僅透過[XPS 檔 API](documents-xps.md)提供支援</span><span class="sxs-lookup"><span data-stu-id="526c8-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="526c8-116">如果您需要在 Microsoft XPS (MSXPS) 與 OpenXPS 之間進行轉換，Microsoft 提供的工具 (XPSConverter.exe) ，可讓您將 MSXPS 格式的檔轉換成 OpenXPS 格式，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="526c8-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="526c8-117">此工具是 Windows 驅動程式套件 (WDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="526c8-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="526c8-118">若要下載 WDK，請參閱 [如何取得 wdk](/windows-hardware/drivers/download-the-wdk)。</span><span class="sxs-lookup"><span data-stu-id="526c8-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="526c8-119">如需有關 OpenXPS 和 Windows 8 的詳細資訊，請參閱 [Windows 中的 OpenXPS 支援](/windows-hardware/drivers/print/driver-support-for-openxps)。</span><span class="sxs-lookup"><span data-stu-id="526c8-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="526c8-120">**XPS 檔 API**</span><span class="sxs-lookup"><span data-stu-id="526c8-120">**XPS Document API**</span></span>

    <span data-ttu-id="526c8-121">XPS 檔 API 是支援 XPS OM 的原生 Windows API。</span><span class="sxs-lookup"><span data-stu-id="526c8-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="526c8-122">XPS 檔 API 是在 Windows 7 中引進的，可用於使用者模式程式和 XPSDrv 印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="526c8-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="526c8-123">如需詳細資訊，請參閱 XPS 檔 API 和 [Xps 數位簽章 api](xps-digital-signatures.md)。</span><span class="sxs-lookup"><span data-stu-id="526c8-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="526c8-124">\*Windows Vista （含 Service Pack 2） (SP2) 搭配 windows Vista 和 windows Server 2008 （含 SP2）的平臺更新（使用 Windows Server 2008 的平臺更新），也支援 XPS 檔 API。</span><span class="sxs-lookup"><span data-stu-id="526c8-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="526c8-125">如需 Windows Vista 平臺更新或 Windows Server 2008 平臺更新的詳細資訊，請參閱 [Windows vista 的平臺更新。](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span><span class="sxs-lookup"><span data-stu-id="526c8-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="526c8-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="526c8-126">**.NET Framework**</span></span>

    <span data-ttu-id="526c8-127">.NET Framework 將 XPS 檔支援提供給使用者模式、managed 程式碼程式。</span><span class="sxs-lookup"><span data-stu-id="526c8-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="526c8-128">Windows XP Service Pack 2 (SP2) 和更新版本的 Windows 用戶端作業系統，以及 Windows Server 2003 （含 Service Pack 2） (SP2) 和更新版本的 Windows server 作業系統都支援 .NET Framework 3.0。</span><span class="sxs-lookup"><span data-stu-id="526c8-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="526c8-129">Windows 用戶端作業系統的 windows XP 版本以及 Windows Server 2003 和更新版本的 Windows server 作業系統都支援 .NET Framework 3.5。</span><span class="sxs-lookup"><span data-stu-id="526c8-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="526c8-130">我們建議您使用 .NET Framework 在用戶端應用程式中建立 XPS 檔，而不是在伺服器應用程式中使用，除非應用程式是以用戶端應用程式的方式定期結束。</span><span class="sxs-lookup"><span data-stu-id="526c8-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="526c8-131">如需 .NET Framework 中檔支援的詳細資訊，請參閱 [Windows Presentation Foundation 檔](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="526c8-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="526c8-132">若要在程式中使用 XPS 檔，請使用原生 XPS 檔 API 或 .NET Framework;不支援在相同的程式中同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="526c8-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="526c8-133">本節內容</span><span class="sxs-lookup"><span data-stu-id="526c8-133">In This Section</span></span>

<span data-ttu-id="526c8-134">本節說明 Microsoft Windows 支援的原生 Windows 檔技術。</span><span class="sxs-lookup"><span data-stu-id="526c8-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



| <span data-ttu-id="526c8-135">檔技術</span><span class="sxs-lookup"><span data-stu-id="526c8-135">Document technology</span></span>                                                                   | <span data-ttu-id="526c8-136">描述</span><span class="sxs-lookup"><span data-stu-id="526c8-136">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="526c8-137">XPS 檔 API</span><span class="sxs-lookup"><span data-stu-id="526c8-137">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="526c8-138">提供電子紙張的可信任格式。</span><span class="sxs-lookup"><span data-stu-id="526c8-138">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="526c8-139">本節所述的 XPS 檔 API 可讓程式和 XPSDrv 列印驅動程式存取 XPS 檔的內容和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="526c8-139">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="526c8-140">XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="526c8-140">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="526c8-141">啟用檔簽署、簽署簽署者的身分識別，以及指出 XPS 檔在簽署之後是否已經變更。</span><span class="sxs-lookup"><span data-stu-id="526c8-141">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="526c8-142">XPS 檔詞彙</span><span class="sxs-lookup"><span data-stu-id="526c8-142">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="526c8-143">[Xps 檔 api](documents-xps.md)和[XPS 數位簽章 api](xps-digital-signatures.md)所使用的詞彙定義。</span><span class="sxs-lookup"><span data-stu-id="526c8-143">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="526c8-144">XPS 檔工具</span><span class="sxs-lookup"><span data-stu-id="526c8-144">XPS Document Tools</span></span>

<span data-ttu-id="526c8-145">下列工具可協助您進行 XPS 檔檔案的測試和疑難排解。</span><span class="sxs-lookup"><span data-stu-id="526c8-145">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="526c8-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="526c8-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="526c8-147">測試檔案對 XML 檔規格 (XPS) 和開放式封裝慣例 (OPC) 規格的符合性。</span><span class="sxs-lookup"><span data-stu-id="526c8-147">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="526c8-148">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="526c8-148">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="526c8-149">一種命令提示字元工具，可分析 XPS 檔檔是否與 XPS 1.0 規格相容。</span><span class="sxs-lookup"><span data-stu-id="526c8-149">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="526c8-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="526c8-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="526c8-151">檢查 PrintTicket 和 PrintCapabilities 檔有效性的工具。</span><span class="sxs-lookup"><span data-stu-id="526c8-151">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="526c8-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="526c8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="526c8-153">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="526c8-153">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="526c8-154">包裝</span><span class="sxs-lookup"><span data-stu-id="526c8-154">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="526c8-155">列印</span><span class="sxs-lookup"><span data-stu-id="526c8-155">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="526c8-156">[列印範例程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="526c8-156">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 

