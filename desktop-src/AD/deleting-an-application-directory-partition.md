---
title: 刪除應用程式目錄分割
description: 刪除表示應用程式目錄分割的交互參照物件，以刪除應用程式目錄分割。
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- 刪除應用程式目錄分割廣告
- 應用程式目錄分割廣告，刪除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681676"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="535f7-105">刪除應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="535f7-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="535f7-106">刪除表示應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件，以刪除應用程式目錄分割。</span><span class="sxs-lookup"><span data-stu-id="535f7-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="535f7-107">將 **交叉交叉** 物件的刪除複寫到具有應用程式目錄分割複本的網域控制站時，KCC 會刪除應用程式目錄分割的本機複本。</span><span class="sxs-lookup"><span data-stu-id="535f7-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="535f7-108">最後會刪除應用程式目錄分割的所有複本。</span><span class="sxs-lookup"><span data-stu-id="535f7-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="535f7-109">刪除 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件時，Active Directory 伺服器將會刪除建立應用程式目錄分割時所建立的 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件，以及刪除應用程式目錄分割中的所有物件。</span><span class="sxs-lookup"><span data-stu-id="535f7-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="535f7-110">當應用程式目錄分割中的物件被刪除時，不會將它們全部刪除。</span><span class="sxs-lookup"><span data-stu-id="535f7-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="535f7-111">刪除應用程式目錄分割時，很難將它還原。</span><span class="sxs-lookup"><span data-stu-id="535f7-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="535f7-112">若要還原應用程式目錄分割，必須還原具有應用程式目錄分割複本的備份，找出代表應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件，並以系統授權方式還原 **交叉引用** 物件。</span><span class="sxs-lookup"><span data-stu-id="535f7-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="535f7-113">**若要刪除應用程式目錄分割及其複本，請執行下列步驟**</span><span class="sxs-lookup"><span data-stu-id="535f7-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="535f7-114">在 [資料分割] 容器中搜尋具有與應用程式目錄分割的辨別名稱相等的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件。</span><span class="sxs-lookup"><span data-stu-id="535f7-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="535f7-115">刪除 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。</span><span class="sxs-lookup"><span data-stu-id="535f7-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="535f7-116">如需詳細資訊，請參閱 [刪除應用程式目錄分割的範例程式碼](example-code-for-deleting-an-application-directory-partition.md)。</span><span class="sxs-lookup"><span data-stu-id="535f7-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 