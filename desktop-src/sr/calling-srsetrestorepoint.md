---
title: 呼叫 SRSetRestorePoint
description: 應用程式可以先建立還原點，然後才會造成重大的系統變更，例如安裝、卸載或功能更新。
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b877c4fe73bcedad363bb4c9cc770a9638550dbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674855"
---
# <a name="calling-srsetrestorepoint"></a><span data-ttu-id="8c33d-103">呼叫 SRSetRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8c33d-103">Calling SRSetRestorePoint</span></span>

<span data-ttu-id="8c33d-104">應用程式可以先建立還原點，然後才會造成重大的系統變更，例如安裝、卸載或功能更新。</span><span class="sxs-lookup"><span data-stu-id="8c33d-104">An application can create a restore point before it causes a significant system change, such as an install, uninstall, or feature update.</span></span>

<span data-ttu-id="8c33d-105">安裝程式應在安裝之前建立還原點，方法是呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa)函式，並將 [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa)結構的 **DWEVENTTYPE** 成員設定為 [開始 \_ 系統 \_ 變更]。</span><span class="sxs-lookup"><span data-stu-id="8c33d-105">Installers should create a restore point just prior to installation by calling the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function with the **dwEventType** member of the [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure set to BEGIN\_SYSTEM\_CHANGE.</span></span> <span data-ttu-id="8c33d-106">若要通知系統還原安裝已完成，請呼叫 **SRSetRestorePoint** ，並將 **dwEventType** 設定為 [結束 \_ 系統變更] \_ 。</span><span class="sxs-lookup"><span data-stu-id="8c33d-106">To notify System Restore that the installation has been completed, call **SRSetRestorePoint** with **dwEventType** set to END\_SYSTEM\_CHANGE.</span></span>

<span data-ttu-id="8c33d-107">如果使用者取消應用程式安裝，安裝程式可能會移除安裝開始時所建立的還原點。</span><span class="sxs-lookup"><span data-stu-id="8c33d-107">If the user cancels the application installation, the installer may remove the restore point it created when the installation began.</span></span> <span data-ttu-id="8c33d-108">移除還原點是選擇性的，可防止使用者在取消時，從安裝程式所進行的非不慎變更中復原。</span><span class="sxs-lookup"><span data-stu-id="8c33d-108">Removing the restore point is optional and can prevent the user from recovering from unintentional changes made by the installer during the cancellation.</span></span> <span data-ttu-id="8c33d-109">如果安裝程式要移除還原點，則可以呼叫 [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) 函式，或呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 並將 **dwRestorePointType** 設定為取消作業 \_ 、將 **dwEventType** 設定為 \_ [結束系統變更] \_ ，並將 **llSequenceNumber** 設定為初始呼叫 **SRSetRestorePoint** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="8c33d-109">If the installer is to remove a restore point, it can call the [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) function, or call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) with **dwRestorePointType** set to CANCELLED\_OPERATION, **dwEventType** set to END\_SYSTEM\_CHANGE, and **llSequenceNumber** set to the value returned by the initial call to **SRSetRestorePoint**.</span></span>

<span data-ttu-id="8c33d-110">**Windows 8：  **</span><span class="sxs-lookup"><span data-stu-id="8c33d-110">**Windows 8:  **</span></span>

<span data-ttu-id="8c33d-111">新的登錄機碼可讓應用程式開發人員變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="8c33d-111">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="8c33d-112">應用程式應該建立此金鑰來使用它，因為它不會在系統中之外。</span><span class="sxs-lookup"><span data-stu-id="8c33d-112">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="8c33d-113">如果機碼不存在，則預設會套用下列各項。</span><span class="sxs-lookup"><span data-stu-id="8c33d-113">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="8c33d-114">如果應用程式呼叫 **SRSetRestorePoint** 函式來建立還原點，則 Windows 會在過去24小時內建立任何還原點時，略過建立這個新的還原點。</span><span class="sxs-lookup"><span data-stu-id="8c33d-114">If an application calls the **SRSetRestorePoint** function to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="8c33d-115">系統還原將 [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus)結構的 **IISequenceNumber** 成員設定為先前在當日建立之還原點的序號，並將 **nStatus** 成員的值設定為「**錯誤 \_ 成功**」。</span><span class="sxs-lookup"><span data-stu-id="8c33d-115">System Restore sets the **IISequenceNumber** member of the [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) structure to the sequence number for the restore point created previously in the day and sets the value of the **nStatus** member to **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="8c33d-116">**SRSetRestorePoint** 函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8c33d-116">The **SRSetRestorePoint** function returns **TRUE**.</span></span>

<span data-ttu-id="8c33d-117">開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **SystemRestorePointCreationFrequency** 。</span><span class="sxs-lookup"><span data-stu-id="8c33d-117">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="8c33d-118">此登錄機碼的值可以變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="8c33d-118">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="8c33d-119">此登錄機碼的值可以變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="8c33d-119">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="8c33d-120">如果應用程式呼叫 **SRSetRestorePoint** 來建立還原點，而登錄機碼值為0，則系統還原不會略過建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="8c33d-120">If the application calls **SRSetRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="8c33d-121">如果應用程式呼叫 **SRSetRestorePoint** 來建立還原點，而登錄機碼值是整數 n，則系統還原會在前 N 分鐘內建立任何還原點時，略過建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="8c33d-121">If the application calls **SRSetRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

<span data-ttu-id="8c33d-122">**Windows 8：  **</span><span class="sxs-lookup"><span data-stu-id="8c33d-122">**Windows 8:  **</span></span>

<span data-ttu-id="8c33d-123">在 Windows 8 上執行的系統還原會監視只與系統還原相關的開機磁碟區中的檔案。</span><span class="sxs-lookup"><span data-stu-id="8c33d-123">System Restore running on Windows 8 monitors files in the boot volume that are relevant for system restore only.</span></span> <span data-ttu-id="8c33d-124">如果後續版本的 Windows 會公開快照集，則會刪除在 Windows 8 上執行系統還原所建立之開機磁碟區的快照。</span><span class="sxs-lookup"><span data-stu-id="8c33d-124">Snapshots of the boot volume created by System Restore running on Windows 8 may be deleted if the snapshot is subsequently exposed by an earlier version of Windows.</span></span> <span data-ttu-id="8c33d-125">請注意，雖然只有一個系統磁碟區，但多重開機系統中的每個作業系統都有一個開機磁碟區。</span><span class="sxs-lookup"><span data-stu-id="8c33d-125">Note that although there is only one system volume, there is one boot volume for each operating system in a multi-boot system.</span></span>

<span data-ttu-id="8c33d-126">開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **ScopeSnapshots** 。</span><span class="sxs-lookup"><span data-stu-id="8c33d-126">Developers can write applications that create the **DWORD** value **ScopeSnapshots** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="8c33d-127">如果此登錄機碼值為0，系統還原會以與舊版 Windows 相同的方式，建立開機磁碟區的快照集。</span><span class="sxs-lookup"><span data-stu-id="8c33d-127">If this registry key value is 0, System Restore creates snapshots of the boot volume in the same way as in earlier versions of Windows.</span></span> <span data-ttu-id="8c33d-128">如果刪除此值，系統還原在 Windows 8 上執行時，會繼續建立快照集，以監視只與系統還原相關的開機磁碟區中的檔案。</span><span class="sxs-lookup"><span data-stu-id="8c33d-128">If this value is deleted, System Restore running on Windows 8 resumes creating snapshots that monitor files in the boot volume that are relevant for system restore only.</span></span>

<span data-ttu-id="8c33d-129">如需範例，請參閱 [使用系統還原](using-system-restore.md)。</span><span class="sxs-lookup"><span data-stu-id="8c33d-129">For an example, see [Using System Restore](using-system-restore.md).</span></span>

 

 




