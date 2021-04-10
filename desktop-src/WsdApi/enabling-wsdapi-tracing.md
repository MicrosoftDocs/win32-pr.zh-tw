---
description: WSDAPI 記錄包含可用於尋找 WSDAPI 應用程式失敗根本原因的偵錯工具資訊。
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: 啟用 WSDAPI 追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026540"
---
# <a name="enabling-wsdapi-tracing"></a><span data-ttu-id="0a90b-103">啟用 WSDAPI 追蹤</span><span class="sxs-lookup"><span data-stu-id="0a90b-103">Enabling WSDAPI Tracing</span></span>

<span data-ttu-id="0a90b-104">WSDAPI 記錄包含可用於尋找 WSDAPI 應用程式失敗根本原因的偵錯工具資訊。</span><span class="sxs-lookup"><span data-stu-id="0a90b-104">WSDAPI logs contain debugging information that can be used to find the root cause of WSDAPI application failures.</span></span> <span data-ttu-id="0a90b-105">啟用追蹤時，記錄資訊會儲存在使用者指定位置的 .etl 檔案中。</span><span class="sxs-lookup"><span data-stu-id="0a90b-105">When tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="0a90b-106">您可以將此 etl 檔案傳送給 Microsoft 開發人員支援，以進行根本原因分析。</span><span class="sxs-lookup"><span data-stu-id="0a90b-106">This .etl file can be sent to Microsoft developer support for root cause analysis.</span></span> <span data-ttu-id="0a90b-107">如需聯絡支援的相關資訊，請移至 [https://support.microsoft.com](https://support.microsoft.com) 。</span><span class="sxs-lookup"><span data-stu-id="0a90b-107">For information about contacting support, go to [https://support.microsoft.com](https://support.microsoft.com).</span></span>

<span data-ttu-id="0a90b-108">此程式必須完成兩次：在用戶端上執行一次，並在主機上進行一次。</span><span class="sxs-lookup"><span data-stu-id="0a90b-108">This procedure must be done twice: once on the client, and once on the host.</span></span>

<span data-ttu-id="0a90b-109">**啟用 WSDAPI 追蹤**</span><span class="sxs-lookup"><span data-stu-id="0a90b-109">**To enable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="0a90b-110">使用 [記事本] 或其他文字編輯器，建立具有下列文字的文字檔：</span><span class="sxs-lookup"><span data-stu-id="0a90b-110">Using Notepad or another text editor, create a text file with the following text:</span></span>

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  <span data-ttu-id="0a90b-111">將文字檔儲存為 `C:\temp\traceguids.txt` ，然後關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="0a90b-111">Save the text file as `C:\temp\traceguids.txt` and then close the file.</span></span>
3.  <span data-ttu-id="0a90b-112">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="0a90b-112">Open an elevated command prompt window.</span></span>
4.  <span data-ttu-id="0a90b-113">執行下列命令： **logman.exe create trace wsdlog-o c： \\ temp \\ wsd**</span><span class="sxs-lookup"><span data-stu-id="0a90b-113">Run the following command: **logman.exe create trace wsdlog -o c:\\temp\\wsd**</span></span>
5.  <span data-ttu-id="0a90b-114">執行下列命令： **logman.exe update wsdlog-pf c： \\ temp \\traceguids.txt**</span><span class="sxs-lookup"><span data-stu-id="0a90b-114">Run the following command: **logman.exe update wsdlog -pf c:\\temp\\traceguids.txt**</span></span>
6.  <span data-ttu-id="0a90b-115">執行下列命令： **logman.exe 開始 wsdlog**</span><span class="sxs-lookup"><span data-stu-id="0a90b-115">Run the following command: **logman.exe start wsdlog**</span></span>
7.  <span data-ttu-id="0a90b-116">啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。</span><span class="sxs-lookup"><span data-stu-id="0a90b-116">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>

<span data-ttu-id="0a90b-117">**停用 WSDAPI 追蹤**</span><span class="sxs-lookup"><span data-stu-id="0a90b-117">**To disable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="0a90b-118">開啟提升權限的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="0a90b-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="0a90b-119">執行下列命令： **logman.exe 停止 wsdlog**</span><span class="sxs-lookup"><span data-stu-id="0a90b-119">Run the following command: **logman.exe stop wsdlog**</span></span>

<span data-ttu-id="0a90b-120">一旦已捕捉到應用程式失敗， \* 就可以將 etl 檔案傳送給 Microsoft 支援服務。</span><span class="sxs-lookup"><span data-stu-id="0a90b-120">Once the application failure has been captured, the \*.etl files can be sent to Microsoft support.</span></span> <span data-ttu-id="0a90b-121">這些檔案位於 `C:\temp\wsd_*.etl` 。</span><span class="sxs-lookup"><span data-stu-id="0a90b-121">These files are located in `C:\temp\wsd_*.etl`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a90b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a90b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a90b-123">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="0a90b-123">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="0a90b-124">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="0a90b-124">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



