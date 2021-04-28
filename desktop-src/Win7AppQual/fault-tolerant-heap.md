---
description: 容錯堆積
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: 容錯堆積
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088396"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="24030-103">容錯堆積</span><span class="sxs-lookup"><span data-stu-id="24030-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="24030-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="24030-104">Affected Platforms</span></span>

<span data-ttu-id="24030-105">**用戶端-** Windows 7</span><span class="sxs-lookup"><span data-stu-id="24030-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="24030-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="24030-106">Feature Impact</span></span>

 <span data-ttu-id="24030-107">**嚴重性-** 中</span><span class="sxs-lookup"><span data-stu-id="24030-107">**Severity -** Medium</span></span>  
<span data-ttu-id="24030-108">**頻率-** 低</span><span class="sxs-lookup"><span data-stu-id="24030-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="24030-109">Description</span><span class="sxs-lookup"><span data-stu-id="24030-109">Description</span></span>

<span data-ttu-id="24030-110">容錯堆積 (FTH) 是 Windows 7 的子系統，負責監視應用程式損毀並自主套用緩和措施，以防止每個應用程式的未來損毀。</span><span class="sxs-lookup"><span data-stu-id="24030-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="24030-111">大部分的使用者都可以使用 FTH，而不需要介入或變更其部分。</span><span class="sxs-lookup"><span data-stu-id="24030-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="24030-112">不過，在某些情況下，應用程式開發人員和軟體測試人員可能需要覆寫此系統的預設行為。</span><span class="sxs-lookup"><span data-stu-id="24030-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="24030-113">解決方法</span><span class="sxs-lookup"><span data-stu-id="24030-113">Solution</span></span>

<span data-ttu-id="24030-114">**查看容錯堆積活動**</span><span class="sxs-lookup"><span data-stu-id="24030-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="24030-115">當服務啟動、停止或開始減輕新應用程式的問題時，容錯堆積會記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="24030-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="24030-116">若要檢視此資訊，請遵循這些步驟：</span><span class="sxs-lookup"><span data-stu-id="24030-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="24030-117">按一下 [開始] 功能表。</span><span class="sxs-lookup"><span data-stu-id="24030-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="24030-118">在 [ **電腦** ] 上按一下滑鼠右鍵，然後按一下 [ **管理**]。</span><span class="sxs-lookup"><span data-stu-id="24030-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="24030-119">按一下 [**事件檢視器**  >  **應用程式及服務記錄** 檔]，以將  >  **Microsoft**  >  **Windows > 容錯堆積**</span><span class="sxs-lookup"><span data-stu-id="24030-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="24030-120">查看 FTH 事件。</span><span class="sxs-lookup"><span data-stu-id="24030-120">View FTH Events.</span></span>

<span data-ttu-id="24030-121">服務停止和啟動事件不包含任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="24030-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="24030-122">FTH Enabled 事件包含處理序識別碼 (PID) 、進程映射名稱和進程實例開始時間。</span><span class="sxs-lookup"><span data-stu-id="24030-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="24030-123">**停用容錯堆積**</span><span class="sxs-lookup"><span data-stu-id="24030-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="24030-124">**注意** 如果您使用登錄編輯程式或使用其他方法不正確地修改登錄，可能會發生嚴重的問題。</span><span class="sxs-lookup"><span data-stu-id="24030-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="24030-125">這些問題可能需要您重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="24030-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="24030-126">Microsoft 無法保證可以解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="24030-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="24030-127">您必須自行承擔修改登錄的風險。</span><span class="sxs-lookup"><span data-stu-id="24030-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="24030-128">若要在系統上完全停用容錯堆積，請將 REG \_ DWORD 值 **HKLM \\ Software \\ Microsoft \\ FTH \\ Enabled** 設定為 **0**。</span><span class="sxs-lookup"><span data-stu-id="24030-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="24030-129">變更此值之後，請重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="24030-129">After changing this value, restart the system.</span></span> <span data-ttu-id="24030-130">新的應用程式將不再啟用 FTH。</span><span class="sxs-lookup"><span data-stu-id="24030-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="24030-131">**重設 FTH 所追蹤的應用程式清單**</span><span class="sxs-lookup"><span data-stu-id="24030-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="24030-132">容錯堆積是自我管理的，而且如果在指定的應用程式中沒有有效防護措施，則會自動停止套用。</span><span class="sxs-lookup"><span data-stu-id="24030-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="24030-133">但是，如果您需要重設 FTH 可減輕問題的應用程式清單 (例如，如果您要測試應用程式，而且需要重現 FTH 正在) 緩和的損毀，您可以從提升許可權的命令提示字元執行下列命令：  **Rundll32.exe fthsvc.dll、FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="24030-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="24030-134">**注意** 執行此命令將會清除所有 FTH 的應用程式，因此在執行此命令之後，目前正常運作的應用程式可能會開始損毀。</span><span class="sxs-lookup"><span data-stu-id="24030-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



