---
description: Windows Driver Model (WDM) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: 從設備磁碟機存取資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a59b59116ca0f71178fb2faed290d6bc76c9d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985141"
---
# <a name="accessing-data-from-device-drivers"></a><span data-ttu-id="dc15a-103">從設備磁碟機存取資料</span><span class="sxs-lookup"><span data-stu-id="dc15a-103">Accessing Data from Device Drivers</span></span>

<span data-ttu-id="dc15a-104">Windows Driver Model (WDM) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。</span><span class="sxs-lookup"><span data-stu-id="dc15a-104">The Windows Driver Model (WDM) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="dc15a-105">硬體驅動程式的類別位於 \\ \\ 根 \\ wmi 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="dc15a-105">The classes for hardware drivers reside in the \\\\root\\wmi namespace.</span></span>

<span data-ttu-id="dc15a-106">對於撰寫設備磁碟機和對設備磁碟機資料有興趣的系統管理員而言，WDM 提供者很感興趣。</span><span class="sxs-lookup"><span data-stu-id="dc15a-106">The WDM provider is of interest to those who write device drivers and to administrators who are interested in device driver data.</span></span>

<span data-ttu-id="dc15a-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="dc15a-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="dc15a-108">設備磁碟機寫入器的資訊</span><span class="sxs-lookup"><span data-stu-id="dc15a-108">Information for Device Driver Writers</span></span>](#information-for-device-driver-writers)
-   [<span data-ttu-id="dc15a-109">驅動程式資料的系統管理員和使用者資訊</span><span class="sxs-lookup"><span data-stu-id="dc15a-109">Information for Administrators and Users of Driver Data</span></span>](#information-for-administrators-and-users-of-driver-data)
-   [<span data-ttu-id="dc15a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc15a-110">Related topics</span></span>](#related-topics)

## <a name="information-for-device-driver-writers"></a><span data-ttu-id="dc15a-111">設備磁碟機寫入器的資訊</span><span class="sxs-lookup"><span data-stu-id="dc15a-111">Information for Device Driver Writers</span></span>

<span data-ttu-id="dc15a-112">當 WDM 提供者從設備磁碟機可執行檔中解壓縮二進位 MOF 時，會建立與特定設備磁碟機相關的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="dc15a-112">WMI classes related to a specific device driver are created when the WDM provider extracts the binary MOF from the device driver executable file.</span></span> <span data-ttu-id="dc15a-113">每次啟動 WMI、安裝新的設備磁碟機，或刪除特定驅動程式的 [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) 實例時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="dc15a-113">This takes place whenever WMI is started, a new device driver is installed, or the instance of [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) for a particular driver is deleted.</span></span> <span data-ttu-id="dc15a-114">藉由檢查 Wmiprov，您可以判斷在解壓縮二進位 MOF 檔案時，是否發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc15a-114">By checking Wmiprov.log, you can determine if an error resulting in failure occurred while extracting the binary MOF file.</span></span> <span data-ttu-id="dc15a-115">[Mofcomp.exe](mofcomp.md)錯誤的詳細資料會在 mofcomp.exe 中報告。</span><span class="sxs-lookup"><span data-stu-id="dc15a-115">Details of [mofcomp](mofcomp.md) errors are reported in Mofcomp.log.</span></span> <span data-ttu-id="dc15a-116">如需詳細資訊，請參閱 [WMI 記錄](wmi-log-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="dc15a-116">For more information, see [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="dc15a-117">基於效能的考慮，由於 WDM 提供者啟動或停止，因此，WDM 提供者不會在建立或刪除類別時產生事件。</span><span class="sxs-lookup"><span data-stu-id="dc15a-117">For performance reasons, the WDM provider does not generate events while creating or deleting classes due to a WDM provider starting or stopping.</span></span>

<span data-ttu-id="dc15a-118">WDM 提供者會將所有 WNODE 的資料轉換成類別資訊。</span><span class="sxs-lookup"><span data-stu-id="dc15a-118">The WDM provider transforms all WNODE data into class information.</span></span> <span data-ttu-id="dc15a-119">如果將資料從 WNODE 轉換成類別資料時遇到錯誤，則會在 Wmiprov 中報告此標頭，並以與記憶體傾印相同的格式轉譯位元組。</span><span class="sxs-lookup"><span data-stu-id="dc15a-119">If an error is encountered when transforming the data from WNODE to class data, it is reported in Wmiprov.log with the header formatted and bytes rendered in the same form as a memory dump.</span></span>

<span data-ttu-id="dc15a-120">在將 WDM 提供者卸載並重載之前，對驅動程式安全性設定所做的變更不會生效。</span><span class="sxs-lookup"><span data-stu-id="dc15a-120">Changes made to driver security settings do not take effect until the WDM provider is unloaded and reloaded.</span></span> <span data-ttu-id="dc15a-121">如需詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dc15a-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="dc15a-122">WMI 也可以讓硬體驅動程式使用高效能計數器。</span><span class="sxs-lookup"><span data-stu-id="dc15a-122">WMI can also make high-performance counters for hardware drivers available.</span></span> <span data-ttu-id="dc15a-123">如需有關建立高效能類別以及在 Perfmon 系統監視器中顯示資料的詳細資訊，請參閱 [改善執行個體提供者的效率](improving-the-efficiency-of-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dc15a-123">For more information about creating high-performance classes and displaying data in Perfmon System Monitor, see [Improving the Efficiency of an Instance Provider](improving-the-efficiency-of-an-instance-provider.md).</span></span> <span data-ttu-id="dc15a-124">如需有關撰寫啟用 WMI 之設備磁碟機的詳細資訊，請參閱 [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="dc15a-124">For more information about writing WMI-enabled device drivers, see [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx).</span></span> <span data-ttu-id="dc15a-125">如需 MOF 檔案中的 WDM 特定限定詞的詳細資訊，請參閱 [**Wdm 提供者專屬的限定詞**](qualifiers-specific-to-the-wdm-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dc15a-125">For more information about WDM specific qualifiers in the MOF file, see [**Qualifiers Specific to the WDM Provider**](qualifiers-specific-to-the-wdm-provider.md).</span></span>

## <a name="information-for-administrators-and-users-of-driver-data"></a><span data-ttu-id="dc15a-126">驅動程式資料的系統管理員和使用者資訊</span><span class="sxs-lookup"><span data-stu-id="dc15a-126">Information for Administrators and Users of Driver Data</span></span>

<span data-ttu-id="dc15a-127">列出 [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) 類別的實例會提供系統中的驅動程式清單，以及有關 WDM 提供者是否成功編譯每個驅動程式之 mof 的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc15a-127">Listing the instances of the [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) class provides a list of the drivers in the system and information about whether the WDM provider succeeded in compiling the MOFs for each driver.</span></span> <span data-ttu-id="dc15a-128">您可以藉由刪除代表該驅動程式的 WMIBinaryMofResource 實例，來強制提供者重新編譯和重新產生驅動程式的類別。</span><span class="sxs-lookup"><span data-stu-id="dc15a-128">You can force the provider to recompile and regenerate the classes for a driver by deleting the instance of WMIBinaryMofResource that represents that driver.</span></span> <span data-ttu-id="dc15a-129">[Mofcomp.exe](mofcomp.md)錯誤的詳細資料會在 mofcomp.exe 中報告。</span><span class="sxs-lookup"><span data-stu-id="dc15a-129">Details of [mofcomp](mofcomp.md) errors are reported in the Mofcomp.log.</span></span>

<span data-ttu-id="dc15a-130">如果 WMI 命名空間已損毀，則可以將它刪除並重新開啟，以強制執行 WDM 重建驅動程式類別。</span><span class="sxs-lookup"><span data-stu-id="dc15a-130">If the WMI namespace is corrupted, it can be deleted and reopened to force WDM to rebuild the driver classes.</span></span> <span data-ttu-id="dc15a-131">如需有關開啟命名空間的詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。</span><span class="sxs-lookup"><span data-stu-id="dc15a-131">For more information about opening a namespace, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

<span data-ttu-id="dc15a-132">驅動程式類別有時可能會在驅動程式載入中斷或其他異常操作時發生「擱置」。</span><span class="sxs-lookup"><span data-stu-id="dc15a-132">Driver classes can occasionally get "stranded" if driver loading is interrupted or other abnormal operations occur.</span></span> <span data-ttu-id="dc15a-133">當安裝新的驅動程式或 **軟體 \\ Microsoft \\ WBEM \\ WDMProvider** 登錄機碼值 **PROCESSSTRANDEDCLASSES** 設定為 **TRUE** 時，WDM 提供者只會搜尋和清除「擱置」類別。</span><span class="sxs-lookup"><span data-stu-id="dc15a-133">The WDM provider will only search for and clean up "stranded" classes when a new driver is installed or when the **Software\\Microsoft\\WBEM\\WDMProvider** registry key value **ProcessStrandedClasses** is set to **TRUE**.</span></span> <span data-ttu-id="dc15a-134">將此值設定為 **TRUE** 會使 WMI 啟動效能變慢，因為清除作業。</span><span class="sxs-lookup"><span data-stu-id="dc15a-134">Setting this value to **TRUE** slows WMI startup performance because of the cleanup operation.</span></span> <span data-ttu-id="dc15a-135">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="dc15a-135">The default value is **FALSE**.</span></span> <span data-ttu-id="dc15a-136">當 \\ 第一次開啟「根 Wmi」命名空間時，WDM 提供者只會檢查這個登錄值。</span><span class="sxs-lookup"><span data-stu-id="dc15a-136">The WDM provider only checks this registry value when the "Root\\Wmi" namespace is opened for the first time.</span></span>

<span data-ttu-id="dc15a-137">如果對 WDM 設備磁碟機進行安全性變更，在將 WDM 提供者卸載並重載之前，變更將不會生效。</span><span class="sxs-lookup"><span data-stu-id="dc15a-137">If security changes are made to a WDM device driver, the changes will not go into effect until the WDM provider is unloaded and reloaded.</span></span> <span data-ttu-id="dc15a-138">Windows 管理服務必須停止並重新啟動，才能完成此動作。</span><span class="sxs-lookup"><span data-stu-id="dc15a-138">The Windows Management service must be stopped and restarted to accomplish this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc15a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc15a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc15a-140">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="dc15a-140">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
