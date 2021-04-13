---
description: 交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: '交易式 NTFS (TxF) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510904"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="3cb5b-103">交易式 NTFS (TxF) </span><span class="sxs-lookup"><span data-stu-id="3cb5b-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="3cb5b-104">\[Microsoft 強烈建議開發人員利用替代方法來達成您的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="3cb5b-105">針對 TxF 開發的許多案例，都可以透過更簡單且更容易使用的技術來達成。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="3cb5b-106">此外，Microsoft Windows 的未來版本可能不提供 TxF。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="3cb5b-107">如需詳細資訊以及 TxF 的替代方案，請參閱 [使用交易式 NTFS 的替代方案](deprecation-of-txf.md)。\]</span><span class="sxs-lookup"><span data-stu-id="3cb5b-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="3cb5b-108">目的</span><span class="sxs-lookup"><span data-stu-id="3cb5b-108">Purpose</span></span>

<span data-ttu-id="3cb5b-109">交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="3cb5b-110">TxF 交易可透過跨失敗保護資料完整性來提高應用程式的可靠性，並大幅減少錯誤處理常式代碼的數量，以簡化應用程式開發。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="3cb5b-111">TxF 使用 [核心交易管理員](/windows/desktop/Ktm/kernel-transaction-manager-portal) 所提供的交易架構 (KTM) 。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="3cb5b-112">這可讓 TxF 檔案作業成為牽涉到其他資料來源之交易的一部分，例如 SQL Server 和交易登錄 (TxR) 。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3cb5b-113">適用時</span><span class="sxs-lookup"><span data-stu-id="3cb5b-113">Where applicable</span></span>

<span data-ttu-id="3cb5b-114">應用程式可以使用 TxF 來保存由於未預期的錯誤狀況所造成之資料的完整性，並藉由在進行變更時隔離您的變更，協助解決並行檔案系統使用者案例。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3cb5b-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="3cb5b-115">Developer audience</span></span>

<span data-ttu-id="3cb5b-116">使用 TxF 之前，您應該具備使用 KTM 或 [分散式交易協調器 (DTC) ](/previous-versions/windows/desktop/ms684146(v=vs.85))之交易的實用知識。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3cb5b-117">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="3cb5b-117">Run-time requirements</span></span>

<span data-ttu-id="3cb5b-118">從 Windows Vista 開始，可以使用 TxF。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3cb5b-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="3cb5b-119">In this section</span></span>



| <span data-ttu-id="3cb5b-120">主題</span><span class="sxs-lookup"><span data-stu-id="3cb5b-120">Topic</span></span>                                                    | <span data-ttu-id="3cb5b-121">描述</span><span class="sxs-lookup"><span data-stu-id="3cb5b-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cb5b-122">關於</span><span class="sxs-lookup"><span data-stu-id="3cb5b-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="3cb5b-123">交易式 NTFS 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="3cb5b-124">參考</span><span class="sxs-lookup"><span data-stu-id="3cb5b-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="3cb5b-125">函數、資料結構、列舉和其他程式設計項目的檔。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

