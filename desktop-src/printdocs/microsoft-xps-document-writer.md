---
description: Microsoft XPS Document Writer (MXDW) 是一種列印到檔的驅動程式，可讓 Windows 應用程式在 windows XP Service Pack 2) SP2 (開始的 Windows 版本上，建立 XML 檔規格 (XPS) 檔檔。
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: 'Microsoft XPS Document Writer (MXDW) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975298"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="4d220-103">Microsoft XPS Document Writer (MXDW) </span><span class="sxs-lookup"><span data-stu-id="4d220-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="4d220-104">Microsoft XPS Document Writer (MXDW) 是一種列印到檔的驅動程式，可讓 Windows 應用程式在 windows XP Service Pack 2) SP2 (開始的 Windows 版本上，建立 XML 檔規格 (XPS) 檔檔。</span><span class="sxs-lookup"><span data-stu-id="4d220-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="4d220-105">使用 MXDW 讓 Windows 應用程式可以將其內容儲存為 XPS 檔，而不需要變更應用程式的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="4d220-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4d220-106">使用時機</span><span class="sxs-lookup"><span data-stu-id="4d220-106">When to Use</span></span>

<span data-ttu-id="4d220-107">如果您想要從 Windows 應用程式建立 XPS 檔，而該檔沒有將其內容儲存為 XPS 檔的選項，您可以選取 [MXDW]。</span><span class="sxs-lookup"><span data-stu-id="4d220-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="4d220-108">身為應用程式開發人員，當您的應用程式未提供儲存為 XPS 檔的選項時，建議您 MXDW 想要建立 XPS 檔的使用者。</span><span class="sxs-lookup"><span data-stu-id="4d220-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="4d220-109">如需有關 XML 檔規格和 XPS 檔的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) 和 [Xps 規格及授權下載](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。</span><span class="sxs-lookup"><span data-stu-id="4d220-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="4d220-110">MXDW 會自動安裝在 windows Vista 和更新版本的 Windows 上，而且可以在 Windows XP SP2 和 Windows Server 2003 上下載和安裝。</span><span class="sxs-lookup"><span data-stu-id="4d220-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="4d220-111">安裝</span><span class="sxs-lookup"><span data-stu-id="4d220-111">Installation</span></span>

<span data-ttu-id="4d220-112">在 Windows Vista 和更新版本的 Windows 上，系統會在安裝作業系統時自動安裝 MXDW。</span><span class="sxs-lookup"><span data-stu-id="4d220-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="4d220-113">**WINDOWS XP SP2 和 Windows Server 2003**：從 [Microsoft 下載中心](https://www.microsoft.com/downloads/en/default.aspx)下載並安裝 .NET Framework 3.0 或 XPS 基本套件。</span><span class="sxs-lookup"><span data-stu-id="4d220-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="4d220-114">如何使用</span><span class="sxs-lookup"><span data-stu-id="4d220-114">How to Use</span></span>

<span data-ttu-id="4d220-115">安裝時，MXDW 會在應用程式所顯示的 [列印] 對話方塊中顯示為可用的列印佇列。</span><span class="sxs-lookup"><span data-stu-id="4d220-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="4d220-116">將 MXDW 選取為印表機時，系統會提示使用者輸入檔案名，將其建立為可捕獲應用程式列印輸出的 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="4d220-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="4d220-117">下圖顯示在 [Windows Vista 一般列印] 對話方塊中選取為 [印表機] 的 MXDW。</span><span class="sxs-lookup"><span data-stu-id="4d220-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![[列印] 對話方塊的影像，其中顯示 microsoft xps document writer (mxdw 的選取專案) ](images/choosingmxdwinvista.gif)

<span data-ttu-id="4d220-119">應用程式開發人員可以使用 [MXDW 設定](mxdw-configuration-settings.md)，自訂 MXDW 的輸出。</span><span class="sxs-lookup"><span data-stu-id="4d220-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d220-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d220-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d220-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4d220-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="4d220-122">XPS 規格與授權下載</span><span class="sxs-lookup"><span data-stu-id="4d220-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="4d220-123">[isXPS 一致性工具](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d220-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4d220-124">MXDW 設定</span><span class="sxs-lookup"><span data-stu-id="4d220-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
