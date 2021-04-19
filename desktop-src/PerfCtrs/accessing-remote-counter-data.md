---
<span data-ttu-id="18ee4-101">描述：若要存取遠端電腦上的計數器資料：遠端電腦必須啟用遠端登入服務。必須在 Windows 防火牆設定中選取檔案和列印共用例外狀況。 Windows Vista 之前：預設會啟用遠端登入服務。</span><span class="sxs-lookup"><span data-stu-id="18ee4-101">description: To access counter data on a remote computer:The remote computer must have the Remote Registry service enabled.The File and Print Sharing exception must be selected in Windows Firewall Settings.Prior to Windows Vista:  The Remote Registry service is enabled by default.</span></span>
<span data-ttu-id="18ee4-102">assetid： 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title：存取遠端計數器 Data ms. 主題：文章 ms. 日期：08/17/2020</span><span class="sxs-lookup"><span data-stu-id="18ee4-102">ms.assetid: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: Accessing Remote Counter Data ms.topic: article ms.date: 08/17/2020</span></span>
---

# <a name="accessing-remote-counter-data"></a><span data-ttu-id="18ee4-103">存取遠端計數器資料</span><span class="sxs-lookup"><span data-stu-id="18ee4-103">Accessing Remote Counter Data</span></span>

<span data-ttu-id="18ee4-104">若要存取遠端電腦上的計數器資料：</span><span class="sxs-lookup"><span data-stu-id="18ee4-104">To access counter data on a remote computer:</span></span>

- <span data-ttu-id="18ee4-105">遠端電腦必須啟用遠端登入服務。</span><span class="sxs-lookup"><span data-stu-id="18ee4-105">The remote computer must have the Remote Registry service enabled.</span></span>
- <span data-ttu-id="18ee4-106">必須選取 [ **Windows 防火牆設定**] 中的 [檔案 **及列印共用**] 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="18ee4-106">The **File and Print Sharing** exception must be selected in **Windows Firewall Settings**.</span></span>

<span data-ttu-id="18ee4-107">**在 Windows Vista 之前：** 預設會啟用遠端登入服務。</span><span class="sxs-lookup"><span data-stu-id="18ee4-107">**Prior to Windows Vista:** The Remote Registry service is enabled by default.</span></span>

> [!NOTE]
> <span data-ttu-id="18ee4-108">Windows 效能計數器 Api 和工具組含有限的支援，可透過 RPC 提供者的 RPC (存取來自其他機器的效能計數器) 和) 的 V1 提供者的遠端登入 (。</span><span class="sxs-lookup"><span data-stu-id="18ee4-108">Windows Performance Counter APIs and tools include limited support for accessing performance counters from other machines via RPC (for V2 providers) and Remote Registry (for V1 providers).</span></span> <span data-ttu-id="18ee4-109">這項支援通常很難用來驗證控制項， (工具和 Api 只能根據目前的使用者) 和系統設定 (進行驗證必要的端點和服務預設會在大部分的系統上停用) 。</span><span class="sxs-lookup"><span data-stu-id="18ee4-109">This support is often hard to use in terms of authentication controls (the tools and APIs can only authenticate as the current user) as well as in terms of system configuration (the necessary endpoints and services are disabled by default on most systems).</span></span> <span data-ttu-id="18ee4-110">在許多情況下，最好透過 [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) 存取遠端系統的效能計數器，而不是透過內建的遠端存取支援。</span><span class="sxs-lookup"><span data-stu-id="18ee4-110">In many cases, it is better to access the performance counters of remote systems via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) rather than via the built-in remote access support.</span></span>
