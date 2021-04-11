---
description: 核心交易管理員 (KTM) 是交易管理服務。 它讓交易可作為核心物件，並提供交易管理服務給系統元件，例如交易式 NTFS (TxF) 。
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: 關於 KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027456"
---
# <a name="about-ktm"></a><span data-ttu-id="56e4a-104">關於 KTM</span><span class="sxs-lookup"><span data-stu-id="56e4a-104">About KTM</span></span>

<span data-ttu-id="56e4a-105">核心交易管理員 (KTM) 是交易管理服務。</span><span class="sxs-lookup"><span data-stu-id="56e4a-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="56e4a-106">它讓交易可作為核心物件，並提供交易管理服務給系統元件，例如交易式 [NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF) 。</span><span class="sxs-lookup"><span data-stu-id="56e4a-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="56e4a-107">下列主題說明 KTM 的使用和功能：</span><span class="sxs-lookup"><span data-stu-id="56e4a-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="56e4a-108">什麼是交易？</span><span class="sxs-lookup"><span data-stu-id="56e4a-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="56e4a-109">使用交易</span><span class="sxs-lookup"><span data-stu-id="56e4a-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="56e4a-110">撰寫 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="56e4a-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="56e4a-111">與其他 Windows 功能的互通性</span><span class="sxs-lookup"><span data-stu-id="56e4a-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="56e4a-112">KTM 安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="56e4a-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="56e4a-113">KTM 依賴 [通用記錄檔系統](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) 進行其作業。</span><span class="sxs-lookup"><span data-stu-id="56e4a-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="56e4a-114">CLFS 是能夠啟用交易的記錄系統。</span><span class="sxs-lookup"><span data-stu-id="56e4a-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
