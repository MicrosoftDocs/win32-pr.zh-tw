---
description: 在開發安全性支援提供者/驗證套件動態連結程式庫 (SSP/AP DLL) 包含一或多個自訂安全性封裝之後，您必須加以註冊。
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: 註冊 SSP/AP Dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692924"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="8ce3f-103">註冊 SSP/AP Dll</span><span class="sxs-lookup"><span data-stu-id="8ce3f-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="8ce3f-104">在開發 [*安全性支援提供者*](../secgloss/s-gly.md) / [*驗證套件*](../secgloss/a-gly.md)動態連結程式庫 (SSP/AP DLL) 包含一或多個自訂 [*安全性封裝*](../secgloss/s-gly.md)之後，您必須加以註冊。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="8ce3f-105">若要這樣做，請將自訂 SSP/AP DLL 的名稱新增至下列登錄值的資料：</span><span class="sxs-lookup"><span data-stu-id="8ce3f-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="8ce3f-106">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **Lsa** \\ **安全性封裝**</span><span class="sxs-lookup"><span data-stu-id="8ce3f-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="8ce3f-107">此登錄值的資料為不含 ".dll" 副檔名的 SSP/AP Dll 名稱清單。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="8ce3f-108">這份清單的資料類型為 **REG \_ 多重 \_ SZ** ，因此 \\ 清單中每個 DLL 名稱之間必須有 null 字元 ( ' 0 ' ) 。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="8ce3f-109">通常，SSP/AP Dll 會儲存在% systemroot%/system32 目錄中。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="8ce3f-110">如果這是您自訂 SSP/AP DLL 的路徑，則不會將路徑包含為 DLL 名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="8ce3f-111">但是，如果 DLL 位於不同的路徑中，請在名稱中包含 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="8ce3f-112">每次系統啟動時，LSA 都會載入這份清單中的 SSP/AP Dll，並執行 [LSA 模式初始化](lsa-mode-initialization.md)中所述的初始化順序。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="8ce3f-113">註冊自訂安全性套件作為預設的 TLS SSP</span><span class="sxs-lookup"><span data-stu-id="8ce3f-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="8ce3f-114">在開發自訂的 TLS 安全性支援提供者，並如上面所述註冊之後，您也必須將它註冊為「預設的 TLS SSP」。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="8ce3f-115">若要這樣做，請將自訂 SSP 的封裝名稱填入下列登錄值的資料中：</span><span class="sxs-lookup"><span data-stu-id="8ce3f-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="8ce3f-116">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **Lsa** \\ **預設 TLS SSP**</span><span class="sxs-lookup"><span data-stu-id="8ce3f-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="8ce3f-117">此登錄值的資料是 SSP 的封裝名稱，而不是 dll 名稱。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="8ce3f-118">這種類型的資料類型是 **REG \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="8ce3f-119">使用「預設 TLS SSP」的使用者模式應用程式將會使用此處註冊的預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="8ce3f-120">使用「Microsoft 統一安全性通訊協定提供者」或其他特定 TLS SSP 名稱的核心模式應用程式或使用者模式應用程式不會受到這項變更的影響。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="8ce3f-121">此登錄資訊僅適用于 SSP/AP DLL。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="8ce3f-122">如需 (Ssp) 註冊安全性支援提供者的詳細資訊，請參閱 [撰寫和安裝安全性支援提供者](writing-and-installing-a-security-support-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="8ce3f-123">如需有關 SSP/AP 與 SSP Dll 之間差異的詳細資訊，請參閱 [ssp/ap 與](ssp-aps-versus-ssps.md)ssp。</span><span class="sxs-lookup"><span data-stu-id="8ce3f-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ce3f-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ce3f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce3f-125">註冊和安裝安全性套件的限制</span><span class="sxs-lookup"><span data-stu-id="8ce3f-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
