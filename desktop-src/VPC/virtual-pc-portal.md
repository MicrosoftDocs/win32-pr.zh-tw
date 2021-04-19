---
title: Windows Virtual PC
description: 使用 Windows Virtual PC COM 介面建立虛擬機器，並安裝虛擬機器;Windows Virtual PC 是最新的 Microsoft 虛擬化技術。
ms.assetid: d47eee76-059b-43dc-a51f-7c08d932a1c7
keywords:
- Windows Virtual PC Virtual PC
- Windows Virtual PC Virtual PC，首頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9dbe0d05100876ae54d327d1fe7ac8cb53d40c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001082"
---
# <a name="windows-virtual-pc"></a><span data-ttu-id="3be77-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3be77-105">Windows Virtual PC</span></span>

<span data-ttu-id="3be77-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3be77-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3be77-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](../hyperv_v2/windows-virtualization-portal.md)。\]</span><span class="sxs-lookup"><span data-stu-id="3be77-107">Instead, use the [Hyper-V WMI provider (V2)](../hyperv_v2/windows-virtualization-portal.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="3be77-108">目的</span><span class="sxs-lookup"><span data-stu-id="3be77-108">Purpose</span></span>

<span data-ttu-id="3be77-109">本檔提供 Windows Virtual PC COM 介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3be77-109">This documentation provides information about the Windows Virtual PC COM interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3be77-110">適用時</span><span class="sxs-lookup"><span data-stu-id="3be77-110">Where applicable</span></span>

<span data-ttu-id="3be77-111">Windows Virtual PC 是最新的 Microsoft 虛擬化技術;它可讓您直接從 Windows 7 在虛擬 Windows 環境中執行許多生產力應用程式，只需按一下即可。</span><span class="sxs-lookup"><span data-stu-id="3be77-111">Windows Virtual PC is the latest Microsoft virtualization technology; it enables you to run many productivity applications on a virtual Windows environment, with a single click, directly from Windows 7.</span></span> <span data-ttu-id="3be77-112">您可以在 Windows 7 桌上型電腦上建立個別的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3be77-112">You can create separate virtual machines on top of your Windows 7 desktop.</span></span> <span data-ttu-id="3be77-113">每部虛擬機器都是在獨立的獨立軟體環境中，模擬一個完整的硬體系統（從處理器到網路卡），以啟用其他不相容系統的平行作業。</span><span class="sxs-lookup"><span data-stu-id="3be77-113">Each virtual machine emulates a complete hardware system—from processor to network card—in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3be77-114">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="3be77-114">Developer audience</span></span>

<span data-ttu-id="3be77-115">Windows Virtual PC COM 介面適用于建立用戶端應用程式的開發人員，以自動化虛擬機器的部署和操作。</span><span class="sxs-lookup"><span data-stu-id="3be77-115">The Windows Virtual PC COM interfaces are for developers who are creating client applications that automate the deployment and operation of virtual machines.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3be77-116">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="3be77-116">Run-time requirements</span></span>

<span data-ttu-id="3be77-117">Windows Virtual PC 需要下列其中一種 Windows 7 版本： Home Basic、Home Premium、Professional、旗艦版或 Enterprise edition。</span><span class="sxs-lookup"><span data-stu-id="3be77-117">Windows Virtual PC requires one of the following Windows 7 editions - Home Basic, Home Premium, Professional, Ultimate, or Enterprise edition.</span></span>

<span data-ttu-id="3be77-118">若要取得相關的標頭檔和程式庫檔案，請從 [Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)安裝適用于 Windows 7 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="3be77-118">To obtain the related header and library files, install the Windows SDK for Windows 7 from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3be77-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="3be77-119">In this section</span></span>

-   [<span data-ttu-id="3be77-120">Windows Virtual PC 參考</span><span class="sxs-lookup"><span data-stu-id="3be77-120">Windows Virtual PC Reference</span></span>](virtual-pc-reference.md)

## <a name="related-topics"></a><span data-ttu-id="3be77-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3be77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be77-122">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3be77-122">Windows Virtual PC</span></span>](https://www.microsoft.com/windows/virtual-pc/)
</dt> </dl>

 

 