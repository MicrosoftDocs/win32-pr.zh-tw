---
description: 將交易式 NTFS (TxF) 和交易式登錄 (TxR) 。 TxF 允許 NTFS 內的交易式檔案系統作業。 TxR 允許交易登錄作業。 使用交易來協調檔案系統和登錄作業。
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: 核心交易管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990412"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="e69f1-106">核心交易管理員</span><span class="sxs-lookup"><span data-stu-id="e69f1-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="e69f1-107">目的</span><span class="sxs-lookup"><span data-stu-id="e69f1-107">Purpose</span></span>

<span data-ttu-id="e69f1-108">核心交易管理員 (KTM) 可讓您開發使用交易的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e69f1-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="e69f1-109">交易引擎本身是在核心內，但是可以針對核心或使用者模式交易，以及在單一主機或分散式主機之間開發交易。</span><span class="sxs-lookup"><span data-stu-id="e69f1-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="e69f1-110">KTM 用來執行交易式 NTFS (TxF) 和交易式登錄 (TxR) 。</span><span class="sxs-lookup"><span data-stu-id="e69f1-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="e69f1-111">TxF 允許 NTFS 檔案系統內的交易式檔案系統作業。</span><span class="sxs-lookup"><span data-stu-id="e69f1-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="e69f1-112">TxR 允許交易登錄作業。</span><span class="sxs-lookup"><span data-stu-id="e69f1-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="e69f1-113">KTM 可讓用戶端應用程式使用交易來協調檔案系統和登錄作業。</span><span class="sxs-lookup"><span data-stu-id="e69f1-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="e69f1-114">若要開發以 TxF 或 TxR 以外的資源來協調交易的應用程式，您必須先開發一個 Win32 交易感知服務，也稱為「資源管理員」。</span><span class="sxs-lookup"><span data-stu-id="e69f1-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="e69f1-115">Managed 和 COM + 應用程式應使用其原生交易管理員。</span><span class="sxs-lookup"><span data-stu-id="e69f1-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e69f1-116">適用時</span><span class="sxs-lookup"><span data-stu-id="e69f1-116">Where applicable</span></span>

<span data-ttu-id="e69f1-117">KTM 可以搭配 Windows Vista 或 Windows Server 2008 上裝載的應用程式和資源管理員使用。</span><span class="sxs-lookup"><span data-stu-id="e69f1-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e69f1-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e69f1-118">Developer audience</span></span>

<span data-ttu-id="e69f1-119">KTM API 是設計來供 C 和 c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="e69f1-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e69f1-120">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e69f1-120">Run-time requirements</span></span>

<span data-ttu-id="e69f1-121">從 Windows Vista 開始支援 KTM。</span><span class="sxs-lookup"><span data-stu-id="e69f1-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e69f1-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="e69f1-122">In this section</span></span>



| <span data-ttu-id="e69f1-123">主題</span><span class="sxs-lookup"><span data-stu-id="e69f1-123">Topic</span></span>                                     | <span data-ttu-id="e69f1-124">描述</span><span class="sxs-lookup"><span data-stu-id="e69f1-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e69f1-125">關於</span><span class="sxs-lookup"><span data-stu-id="e69f1-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="e69f1-126">有關交易的一般資訊，以及 KTM 提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e69f1-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="e69f1-127">參考</span><span class="sxs-lookup"><span data-stu-id="e69f1-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="e69f1-128">適用于 KTM 的函式、資料結構、列舉和其他程式設計項目的檔。</span><span class="sxs-lookup"><span data-stu-id="e69f1-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e69f1-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e69f1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e69f1-130">通用記錄檔系統</span><span class="sxs-lookup"><span data-stu-id="e69f1-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="e69f1-131">交易式 NTFS (TxF) </span><span class="sxs-lookup"><span data-stu-id="e69f1-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="e69f1-132">[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e69f1-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

