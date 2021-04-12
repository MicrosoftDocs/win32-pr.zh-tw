---
title: SYSMON 傳回值
description: 以下是在 Smonmsg 中定義的系統監視器傳回值的清單。
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376145"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="d628e-103">SYSMON 傳回值</span><span class="sxs-lookup"><span data-stu-id="d628e-103">SYSMON Return Values</span></span>

<span data-ttu-id="d628e-104">以下是在 Smonmsg 中定義的系統監視器傳回值的清單。</span><span class="sxs-lookup"><span data-stu-id="d628e-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="d628e-105">傳回值</span><span class="sxs-lookup"><span data-stu-id="d628e-105">Return value</span></span>                                       | <span data-ttu-id="d628e-106">描述</span><span class="sxs-lookup"><span data-stu-id="d628e-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d628e-107">SMON \_ 狀態 \_ DUPL \_ 計數器 \_ 路徑 (0xC0001388) </span><span class="sxs-lookup"><span data-stu-id="d628e-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="d628e-108">計數器集合已包含指定的計數器。</span><span class="sxs-lookup"><span data-stu-id="d628e-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="d628e-109">SMON \_ STATUS \_ NO \_ SYSMON \_ OBJECT (0xC0001389) </span><span class="sxs-lookup"><span data-stu-id="d628e-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="d628e-110">這些設定不包含任何完整的系統監視器 HTML 物件。</span><span class="sxs-lookup"><span data-stu-id="d628e-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="d628e-111">SMON \_ 狀態 \_ 太 \_ 少 \_ 樣本 (0xC000138A) </span><span class="sxs-lookup"><span data-stu-id="d628e-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="d628e-112">指定的記錄檔包含的資料樣本少於兩個。</span><span class="sxs-lookup"><span data-stu-id="d628e-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d628e-113">SMON \_ 狀態 \_ 記錄 \_ 檔 \_ 大小 \_ 限制 (0xC000138B) </span><span class="sxs-lookup"><span data-stu-id="d628e-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="d628e-114">指定的記錄檔超過系統監視器控制項的大小限制。</span><span class="sxs-lookup"><span data-stu-id="d628e-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="d628e-115">如果目前已選取記錄檔，請選取 [目前的活動] 作為資料來源，以便卸載目前的記錄檔，然後重新選取指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d628e-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="d628e-116">SMON \_ 狀態 \_ 記錄 \_ 檔 \_ 資料 \_ 源 (0xC000138C) </span><span class="sxs-lookup"><span data-stu-id="d628e-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="d628e-117">若要在資料來源中加入新的記錄檔，必須將資料來源類型變更為 sysmonLogFiles 以外的類型。</span><span class="sxs-lookup"><span data-stu-id="d628e-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="d628e-118">SMON \_ 狀態 \_ DUPL \_ 記錄 \_ 檔 \_ 路徑 (0xC000138D) </span><span class="sxs-lookup"><span data-stu-id="d628e-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="d628e-119">記錄檔集合已包含指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d628e-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="d628e-120">如需系統監視器所傳回之其他傳回值的描述，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 和 [效能資料](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values)協助程式錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d628e-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 