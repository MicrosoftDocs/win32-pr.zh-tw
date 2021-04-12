---
title: 設定系統還原
description: 系統還原使用 Windows Management Instrumentation (WMI) ，以提供可編寫腳本的方式來設定及使用其功能。 它會在根預設命名空間中公開兩個類別： SystemRestore 和 SystemRestoreConfig \\ 。
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375793"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="97d6a-104">設定系統還原</span><span class="sxs-lookup"><span data-stu-id="97d6a-104">Configuring System Restore</span></span>

<span data-ttu-id="97d6a-105">系統還原使用 [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) ，以提供可編寫腳本的方式來設定及使用其功能。</span><span class="sxs-lookup"><span data-stu-id="97d6a-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="97d6a-106">它會在根預設命名空間中公開兩個類別： [**SystemRestore**](systemrestore.md) 和 [**SystemRestoreConfig**](systemrestoreconfig.md) \\ 。</span><span class="sxs-lookup"><span data-stu-id="97d6a-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="97d6a-107">[**SystemRestore**](systemrestore.md)類別提供下列工作的方法：</span><span class="sxs-lookup"><span data-stu-id="97d6a-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="97d6a-108">停用和啟用監視</span><span class="sxs-lookup"><span data-stu-id="97d6a-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="97d6a-109">列出可用的還原點</span><span class="sxs-lookup"><span data-stu-id="97d6a-109">Listing available restore points</span></span>
-   <span data-ttu-id="97d6a-110">在本機系統上起始還原</span><span class="sxs-lookup"><span data-stu-id="97d6a-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="97d6a-111">正在抓取上次系統還原的狀態</span><span class="sxs-lookup"><span data-stu-id="97d6a-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="97d6a-112">[**SystemRestoreConfig**](systemrestoreconfig.md)類別提供的屬性可用來控制排程的還原點建立頻率，以及每個磁片磁碟機上系統還原所耗用的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="97d6a-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="97d6a-113">這兩個類別都可以使用標準 WMI 技術從遠端存取。</span><span class="sxs-lookup"><span data-stu-id="97d6a-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="97d6a-114">如需 WMI 的完整說明，請參閱 [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)。</span><span class="sxs-lookup"><span data-stu-id="97d6a-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 