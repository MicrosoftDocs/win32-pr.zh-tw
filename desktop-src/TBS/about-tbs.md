---
title: 關於 TB
description: 一種系統服務，可讓您透明共用可信賴平臺模組 (TPM) 資源。
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM 基礎服務 TB、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104185475"
---
# <a name="about-tbs"></a><span data-ttu-id="1caf9-104">關於 TB</span><span class="sxs-lookup"><span data-stu-id="1caf9-104">About TBS</span></span>

<span data-ttu-id="1caf9-105">TPM 基礎服務 (TB) 功能是一種系統服務，可讓您透明共用信賴平臺模組 (TPM) 資源。</span><span class="sxs-lookup"><span data-stu-id="1caf9-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="1caf9-106">它會同時在同一部實體機器上的多個應用程式之間共用 TPM 資源，即使這些應用程式是在不同的虛擬機器上執行也一樣。</span><span class="sxs-lookup"><span data-stu-id="1caf9-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="1caf9-107">從 Windows 8 和 Windows Server 2012 開始，會在所有具有 TPM 的系統上預先安裝 TB。</span><span class="sxs-lookup"><span data-stu-id="1caf9-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="1caf9-108">信賴運算群組 (TCG) 定義了一個可提供密碼編譯功能的可信賴平臺模組，其設計目的是為了在平臺中提供信任。</span><span class="sxs-lookup"><span data-stu-id="1caf9-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="1caf9-109">由於 TPM 是在硬體中執行，因此它具有有限的資源。</span><span class="sxs-lookup"><span data-stu-id="1caf9-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="1caf9-110">TCG 也會定義軟體堆疊，以利用這些資源為應用程式軟體提供受信任的作業。</span><span class="sxs-lookup"><span data-stu-id="1caf9-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="1caf9-111">但是，不會提供與作業系統軟體並存執行 TSS 執行的布建，而作業系統軟體也可能使用 TPM 資源。</span><span class="sxs-lookup"><span data-stu-id="1caf9-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="1caf9-112">TBS 功能可解決此問題，方法是啟用與 TBS 通訊的每個軟體堆疊，以針對可能在電腦上執行的任何其他軟體堆疊使用 TPM 資源檢查。</span><span class="sxs-lookup"><span data-stu-id="1caf9-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="1caf9-113">您可以從取得 TPM 規格和 TCG Software Stack (TSS) 規格 [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) 。</span><span class="sxs-lookup"><span data-stu-id="1caf9-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="1caf9-114">TBS 會實作為跨進程服務，以接受使用 RPC 服務的命令。</span><span class="sxs-lookup"><span data-stu-id="1caf9-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="1caf9-115">動態連結的程式庫會呈現 C 語言介面，並與「TB」服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="1caf9-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="1caf9-116">TB 服務只接受來自本機電腦的 RPC 要求。</span><span class="sxs-lookup"><span data-stu-id="1caf9-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="1caf9-117">TB 的主要目標是：</span><span class="sxs-lookup"><span data-stu-id="1caf9-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="1caf9-118">提供有限 TPM 資源的有效共用，例如金鑰位置、授權會話位置和傳輸位置。</span><span class="sxs-lookup"><span data-stu-id="1caf9-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="1caf9-119">在多個 TPM 軟體堆疊實例之間，提供 TPM 資源的優先順序和同步存取。</span><span class="sxs-lookup"><span data-stu-id="1caf9-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="1caf9-120">跨電源狀態提供適當的 TPM 資源管理。</span><span class="sxs-lookup"><span data-stu-id="1caf9-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="1caf9-121">防止 TPM 軟體堆疊存取應受限制的 TPM 命令，可能是因為平臺限制或系統管理需求。</span><span class="sxs-lookup"><span data-stu-id="1caf9-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="1caf9-122">下圖顯示此 TB 與 TPM 之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="1caf9-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![在核心模式中，在使用者模式與 tpm 之間的 tbs 的關聯性](images/tbs-block-diagram-as11601.png)

 

 




