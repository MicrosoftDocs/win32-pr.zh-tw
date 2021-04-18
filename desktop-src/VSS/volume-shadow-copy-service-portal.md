---
description: 備份磁片區，而系統上的應用程式會繼續寫入磁片區。 快速建立複製所有資料之磁片區的快照 (陰影複製) ，以將應用程式停機時間降到最低。 執行 multivolume 備份。
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: 磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971403"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="d7cbd-105">磁碟區陰影複製服務</span><span class="sxs-lookup"><span data-stu-id="d7cbd-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="d7cbd-106">目的</span><span class="sxs-lookup"><span data-stu-id="d7cbd-106">Purpose</span></span>

<span data-ttu-id="d7cbd-107">磁碟區陰影複製服務 (VSS) 是一組 COM 介面，可在系統上的應用程式繼續寫入磁片區時，利用這些介面來執行架構，以允許進行磁片區備份。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="d7cbd-108">如需系統管理員的 VSS 簡介，請參閱 TechNet Library 中的 [磁碟區陰影複製服務](/windows-server/storage/file-server/volume-shadow-copy-service) 。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d7cbd-109">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="d7cbd-109">Run-time requirements</span></span>

<span data-ttu-id="d7cbd-110">Microsoft Windows XP 及更新版本支援 VSS。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="d7cbd-111">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="d7cbd-112">所有32位 VSS 應用程式 (要求者、提供者和寫入器) 必須以原生32位或64位應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="d7cbd-113">不支援在 WOW64 下執行它們。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="d7cbd-114">如需詳細資訊，請參閱支援的設定 [和限制](usage-conventions.md)。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="d7cbd-115">**Windows Server 2003 和 WINDOWS XP：** 支援在 WOW64 下執行32位 VSS 要求者，但不支援系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="d7cbd-116">不支援在 WOW64 下執行32位 VSS 提供者和寫入器。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="d7cbd-117">在 Windows Vista 和後續版本中，已移除在 WOW64 下執行32位要求者的支援。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="d7cbd-118">在 Windows Server 2003 R2 或 Windows Server 2003 上建立的陰影複製，無法在執行 Windows Server 2008 R2 或 Windows Server 2008 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="d7cbd-119">在 Windows Server 2008 R2 或 Windows Server 2008 上建立的陰影複製無法在執行 Windows Server 2003 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="d7cbd-120">不過，在 Windows Server 2008 上建立的陰影複製可以在執行 Windows Server 2008 R2 的電腦上使用，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d7cbd-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="d7cbd-121">In this section</span></span>



| <span data-ttu-id="d7cbd-122">主題</span><span class="sxs-lookup"><span data-stu-id="d7cbd-122">Topic</span></span>                                                          | <span data-ttu-id="d7cbd-123">描述</span><span class="sxs-lookup"><span data-stu-id="d7cbd-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7cbd-124">概觀</span><span class="sxs-lookup"><span data-stu-id="d7cbd-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="d7cbd-125">描述 VSS 物件模型、備份和還原策略，以及如何建立 VSS 提供者、要求者和寫入器。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="d7cbd-126">參考</span><span class="sxs-lookup"><span data-stu-id="d7cbd-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="d7cbd-127">描述 VSS 類別、資料類型、列舉、函數、介面和結構。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="d7cbd-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="d7cbd-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7cbd-129">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d7cbd-129">Windows Vista and later</span></span>            | <span data-ttu-id="d7cbd-130">VSS 適用于 Microsoft Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d7cbd-131">您可以從 [Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)安裝適用于 windows 7 和 windows Server 2008 R2 的 SDK。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="d7cbd-132">您也可以從 Windows 下載中心下載 [ISO 版本](https://www.microsoft.com/download/details.aspx?id=8442) 的 SDK。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="d7cbd-133">您可以從 [Windows SDK 下載頁面](https://msdn.microsoft.com/windows/bb980924.aspx)下載舊版 SDK。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="d7cbd-134">Windows Server 2003 和 Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7cbd-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="d7cbd-135">您可以從 [Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=23490)下載磁碟區陰影複製服務 7.2 SDK 提供的 VSS。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="d7cbd-136">請注意，Win2003 Obj 目錄下目錄中的64位 vssapi .lib 檔案 \\ 可用於64位版本的 Windows Server 2003 和 WINDOWS XP。</span><span class="sxs-lookup"><span data-stu-id="d7cbd-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
