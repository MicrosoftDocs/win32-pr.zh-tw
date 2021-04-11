---
description: 只有當要求者有一些可用提供者的相關資訊時，才應該選取特定的提供者。
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: 選取提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115140"
---
# <a name="selecting-providers"></a><span data-ttu-id="3d5c0-103">選取提供者</span><span class="sxs-lookup"><span data-stu-id="3d5c0-103">Selecting Providers</span></span>

<span data-ttu-id="3d5c0-104">只有當要求者有一些可用提供者的相關資訊時，才應該選取特定的提供者。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="3d5c0-105">因為這通常不是這種情況，建議要求者提供 GUID \_ Null 做為 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)的提供者識別碼，讓系統根據下列演算法選擇提供者：</span><span class="sxs-lookup"><span data-stu-id="3d5c0-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="3d5c0-106">如果有支援指定磁片區的硬體提供者可供使用，則會予以選取。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="3d5c0-107">如果沒有可用的硬體提供者，則如果指定的磁片區有任何特定的軟體提供者可供使用，則會予以選取。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="3d5c0-108">如果沒有硬體提供者和磁片區專用的軟體提供者，則會選取系統提供者。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="3d5c0-109">不過，要求者可以使用 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)來取得可用提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="3d5c0-110">有了這項資訊，而且只有在備份應用程式對各種提供者有充分的瞭解時，要求者可以提供有效的提供者識別碼給 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="3d5c0-111">請注意，所有磁片區都不需要有相同的提供者。</span><span class="sxs-lookup"><span data-stu-id="3d5c0-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



