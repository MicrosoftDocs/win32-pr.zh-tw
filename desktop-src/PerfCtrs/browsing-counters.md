---
description: 若要顯示對話方塊，以列出電腦上定義的效能物件和計數器，請呼叫 PdhBrowseCounters 函數。
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: 流覽計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969363"
---
# <a name="browsing-counters"></a><span data-ttu-id="124be-103">流覽計數器</span><span class="sxs-lookup"><span data-stu-id="124be-103">Browsing Counters</span></span>

<span data-ttu-id="124be-104">若要顯示對話方塊，以列出電腦上定義的效能物件和計數器，請呼叫 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) 函數。</span><span class="sxs-lookup"><span data-stu-id="124be-104">To display a dialog box that lists the performance objects and counters defined on the computer, call the [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) function.</span></span> <span data-ttu-id="124be-105">此對話方塊可讓使用者流覽和選取效能計數器。</span><span class="sxs-lookup"><span data-stu-id="124be-105">The dialog box lets the user browse and select performance counters.</span></span> <span data-ttu-id="124be-106">您可以使用 [**PDH \_ 流覽 \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) 設定結構來指定對話方塊的設定。</span><span class="sxs-lookup"><span data-stu-id="124be-106">You use the [**PDH\_BROWSE\_DLG\_CONFIG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) structure to specify the configuration of the dialog box.</span></span> <span data-ttu-id="124be-107">例如，您可以將對話方塊設定為傳回一或多個選取專案。</span><span class="sxs-lookup"><span data-stu-id="124be-107">For example, you can configure the dialog to return one selection or multiple selections.</span></span>

<span data-ttu-id="124be-108">在輸入時， **szReturnPathBuffer** 成員會包含在對話方塊中選取的預設效能物件和計數器。</span><span class="sxs-lookup"><span data-stu-id="124be-108">On input, the **szReturnPathBuffer** member contains the default performance object and counter that is selected in the dialog box.</span></span> <span data-ttu-id="124be-109">在輸出時，緩衝區會包含使用者選取的效能物件和計數器。</span><span class="sxs-lookup"><span data-stu-id="124be-109">On output, the buffer contains the performance object and counter that the user selected.</span></span> <span data-ttu-id="124be-110">您也可以使用 **pCallBack** 成員來指定回呼函式，以處理對話方塊所傳回的計數器名稱。</span><span class="sxs-lookup"><span data-stu-id="124be-110">You can also use the **pCallBack** member to specify a callback function to process the counter names returned by the dialog box.</span></span>

<span data-ttu-id="124be-111">請注意， \_ \_ 如果 **bSingleCounterPerDialog** 為 **FALSE** ，且使用者按一下 [關閉] 按鈕，則此對話方塊可能會傳回 PDH 對話方塊，所以您的錯誤處理必須考慮這一點。</span><span class="sxs-lookup"><span data-stu-id="124be-111">Note that this dialog box can return PDH\_DIALOG\_CANCELLED if **bSingleCounterPerDialog** is **FALSE** and the user clicks the Close button, so your error handling would have to account for this.</span></span>

<span data-ttu-id="124be-112">如需使用 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) 函數的範例，請參閱 [流覽效能計數器](browsing-performance-counters.md)。</span><span class="sxs-lookup"><span data-stu-id="124be-112">For an example that uses the [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) function, see [Browsing Performance Counters](browsing-performance-counters.md).</span></span>

<span data-ttu-id="124be-113">若要取得電腦上的效能物件清單，您也可以呼叫 [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="124be-113">To retrieve a list of performance objects on the computer, you can also call the [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) function.</span></span> <span data-ttu-id="124be-114">若要取得效能物件的計數器和實例清單，請呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="124be-114">To retrieve a list of counters and instances for a performance object, call the [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) function.</span></span> <span data-ttu-id="124be-115">您也可以使用這些函數來識別記錄檔中所包含的效能物件和計數器。</span><span class="sxs-lookup"><span data-stu-id="124be-115">You can also use these functions to identify the performance objects and counters contained in a log file.</span></span> <span data-ttu-id="124be-116">對 **PdhEnumObjectItems** 的重複呼叫會傳回相同的計數器和實例清單，直到您先呼叫 **PdhEnumObjects** 重新整理效能物件清單為止。</span><span class="sxs-lookup"><span data-stu-id="124be-116">Repeated calls to **PdhEnumObjectItems** will return the same list of counters and instances until you call **PdhEnumObjects** to refresh the list of performance objects first.</span></span> <span data-ttu-id="124be-117">如需列舉物件和計數器的範例，請參閱 [列舉處理常式物件](enumerating-process-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="124be-117">For an example that enumerates objects and counters, see [Enumerating Process Objects](enumerating-process-objects.md).</span></span>

## <a name="selecting-the-data-source"></a><span data-ttu-id="124be-118">選取資料來源</span><span class="sxs-lookup"><span data-stu-id="124be-118">Selecting the data source</span></span>

<span data-ttu-id="124be-119">您可以搭配使用 [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) 與 [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) ，以提示使用者選取資料來源是即時或從記錄檔，而且如果是記錄檔，則為其名稱。</span><span class="sxs-lookup"><span data-stu-id="124be-119">You can use [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) in conjunction with [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) to prompt the user to select whether the data source is in real-time or from a log file, and, if it is a log file, its name.</span></span> <span data-ttu-id="124be-120">如果您不想要顯示 [資料來源] 對話方塊，您可以呼叫 **PdhSelectDataSource** 來只顯示檔案瀏覽器類別目錄。</span><span class="sxs-lookup"><span data-stu-id="124be-120">If you do not want the data source dialog to be displayed, you can call **PdhSelectDataSource** to display only the file browser catalog.</span></span> <span data-ttu-id="124be-121">若要這樣做，請將 PDH \_ 旗標檔案 \_ \_ 瀏覽器指定 \_ 為 **PdhSelectDataSource** 呼叫的第二個參數。</span><span class="sxs-lookup"><span data-stu-id="124be-121">To do this, specify PDH\_FLAGS\_FILE\_BROWSER\_ONLY as the second parameter of the call to **PdhSelectDataSource**.</span></span>

 

 



