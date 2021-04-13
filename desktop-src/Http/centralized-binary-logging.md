---
title: 集中式二進位記錄
description: 集中式二進位記錄是一種可在伺服器會話上啟用的伺服器端記錄類型。
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314962"
---
# <a name="centralized-binary-logging"></a><span data-ttu-id="40763-103">集中式二進位記錄</span><span class="sxs-lookup"><span data-stu-id="40763-103">Centralized Binary Logging</span></span>

<span data-ttu-id="40763-104">集中式二進位記錄是一種可在伺服器會話上啟用的伺服器端記錄類型。</span><span class="sxs-lookup"><span data-stu-id="40763-104">Centralized binary logging is a type of server side logging that can be enabled on the server session.</span></span> <span data-ttu-id="40763-105">集中式二進位記錄功能可做為伺服器會話下建立之所有 URL 群組的集中式記錄，並允許伺服器會話下的所有 URL 群組將二進位、未格式化的記錄資料傳送至單一記錄檔。</span><span class="sxs-lookup"><span data-stu-id="40763-105">Centralized binary logging functions as a centralized form of logging for all the URL groups created under the server session, and allows all the URL groups under the server session to send binary, unformatted log data to a single log file.</span></span> <span data-ttu-id="40763-106">這種類型的記錄只能在伺服器會話上啟用;無法在 URL 群組上啟用。</span><span class="sxs-lookup"><span data-stu-id="40763-106">This type of logging can be enabled on the server session only; it cannot be enabled on the URL group.</span></span>

## <a name="when-to-use-centralized-binary-logging"></a><span data-ttu-id="40763-107">使用集中式二進位記錄的時機</span><span class="sxs-lookup"><span data-stu-id="40763-107">When to use Centralized Binary Logging</span></span>

<span data-ttu-id="40763-108">當伺服器會話中有多個 URL 群組時，為個別的 URL 群組建立數百個格式化記錄檔，並將記錄資料寫入磁片的程式，可快速取用寶貴的 CPU 和記憶體資源，進而建立效能和擴充性問題。</span><span class="sxs-lookup"><span data-stu-id="40763-108">When the server session has numerous URL groups under it, the process of creating hundreds of formatted log files for individual URL groups and writing the log data to a disk can quickly consume valuable CPU and memory resources, thereby creating performance and scalability issues.</span></span> <span data-ttu-id="40763-109">集中式二進位記錄可將用於記錄的系統資源量降至最低，同時也能為需要的組織提供詳細的記錄資料。</span><span class="sxs-lookup"><span data-stu-id="40763-109">Centralized binary logging minimizes the amount of system resources that are used for logging, while at the same time providing detailed log data for organizations that require it.</span></span>

<span data-ttu-id="40763-110">集中式二進位記錄是一種伺服器會話屬性，在啟用時，會為伺服器會話下的所有 URL 群組設定記錄。</span><span class="sxs-lookup"><span data-stu-id="40763-110">Centralized binary logging is a server session property that, when enabled, configures logging for all of the URL groups under the server session.</span></span> <span data-ttu-id="40763-111">啟用集中式二進位記錄時，無法針對個別的 URL 群組錄製或格式化資料。</span><span class="sxs-lookup"><span data-stu-id="40763-111">When centralized binary logging is enabled, data cannot be recorded or formatted for individual URL groups.</span></span> <span data-ttu-id="40763-112">集中式二進位記錄記錄檔 ( ibl) 副檔名。</span><span class="sxs-lookup"><span data-stu-id="40763-112">The centralized binary logging log file has an Internet binary log (.ibl) file name extension.</span></span> <span data-ttu-id="40763-113">此副檔名可確保文字公用程式不會嘗試開啟並讀取中央二進位記錄記錄檔。</span><span class="sxs-lookup"><span data-stu-id="40763-113">This file name extension ensures that text utilities do not try to open and read the central binary logging log file.</span></span>

## <a name="extracting-data-from-the-centralized-binary-log-file"></a><span data-ttu-id="40763-114">從集中式二進位記錄檔解壓縮資料</span><span class="sxs-lookup"><span data-stu-id="40763-114">Extracting Data from the Centralized Binary Log File</span></span>

<span data-ttu-id="40763-115">執行下列步驟以從原始記錄檔中取出資料：</span><span class="sxs-lookup"><span data-stu-id="40763-115">The following steps are performed to extract data from a raw log file:</span></span>

-   <span data-ttu-id="40763-116">建立工具，從原始檔案尋找並解壓縮您想要的資料，並將資料轉換成格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="40763-116">Create a tool that locates and extracts the data that you want from the raw file and converts the data into formatted text.</span></span> <span data-ttu-id="40763-117">您可以在 MSDN 上的 IIS 6.0 軟體發展工具組中，查看標頭檔和記錄檔格式描述。</span><span class="sxs-lookup"><span data-stu-id="40763-117">You can view a header file and log file format descriptions in the IIS 6.0 Software Development Kit on MSDN.</span></span>
-   <span data-ttu-id="40763-118">使用記錄剖析器工具，從原始檔案解壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="40763-118">Use the Log Parser tool to extract data from the raw file.</span></span> <span data-ttu-id="40763-119">記錄剖析器工具及其隨附的使用者檔包含在 IIS 6.0 資源套件工具中。</span><span class="sxs-lookup"><span data-stu-id="40763-119">The Log Parser tool and its accompanying user documentation are included in the IIS 6.0 Resource Kit Tools.</span></span>

## <a name="centralized-binary-logging-file-format"></a><span data-ttu-id="40763-120">集中式二進位記錄檔案格式</span><span class="sxs-lookup"><span data-stu-id="40763-120">Centralized Binary Logging File Format</span></span>

<span data-ttu-id="40763-121">原始的集中式二進位記錄記錄檔是由固定長度的記錄或包含字串識別碼的索引記錄所組成。</span><span class="sxs-lookup"><span data-stu-id="40763-121">The raw centralized binary logging log file is made up of fixed-length records or index records that contain string identifiers.</span></span> <span data-ttu-id="40763-122">出現索引記錄的原因是，為了盡可能記錄最多的資訊，可變長度的字串欄位會被數位識別碼（索引）取代，這會將可變長度的字串對應至記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40763-122">The index records appear because, in an effort to record as much information as possible, variable-length string fields are replaced by numeric identifiers — indexes — that map the variable-length string to the logged identifier.</span></span>

<span data-ttu-id="40763-123">未經處理的記錄檔不是人類可讀取的檔案，而且無法使用大部分可用的記錄分析器來讀取。</span><span class="sxs-lookup"><span data-stu-id="40763-123">The raw log file is not human-readable, and it cannot be read using most available log analyzers.</span></span> <span data-ttu-id="40763-124">若要從原始記錄檔將資料解壓縮，您可以建立工具來尋找並解壓縮資料，然後將它轉換成格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="40763-124">To extract data from a raw log file, you can create a tool that locates and extracts the data and then converts it into formatted text.</span></span>

<span data-ttu-id="40763-125">如需詳細資訊，請參閱 Microsoft TechNet 上的 [集中式二進位記錄](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) 。</span><span class="sxs-lookup"><span data-stu-id="40763-125">For more information, see [Centralized Binary Logging](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) on Microsoft TechNet.</span></span>

 

 