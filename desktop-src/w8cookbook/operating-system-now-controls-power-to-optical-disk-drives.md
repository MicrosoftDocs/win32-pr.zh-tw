---
title: 作業系統現在可控制磁片磁碟機的電源
description: 作業系統現在可控制磁片磁碟機的電源
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683216"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="fd13c-103">作業系統現在可控制磁片磁碟機的電源</span><span class="sxs-lookup"><span data-stu-id="fd13c-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="fd13c-104">平台</span><span class="sxs-lookup"><span data-stu-id="fd13c-104">Platforms</span></span>

<span data-ttu-id="fd13c-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="fd13c-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fd13c-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd13c-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fd13c-107">Description</span><span class="sxs-lookup"><span data-stu-id="fd13c-107">Description</span></span>

<span data-ttu-id="fd13c-108">在舊版的 Windows 中，當光碟機未使用時，不會管理光碟機的電源。</span><span class="sxs-lookup"><span data-stu-id="fd13c-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="fd13c-109">現在，如果光學磁片磁碟機中沒有媒體 (奇怪的) ，作業系統會關閉光碟機的電源。</span><span class="sxs-lookup"><span data-stu-id="fd13c-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="fd13c-110">這項功能稱為零的強大 (ZPODD) 。</span><span class="sxs-lookup"><span data-stu-id="fd13c-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="fd13c-111">這項功能僅適用于使用超薄 SATA (串列先進技術附件) 連接器的光碟機。</span><span class="sxs-lookup"><span data-stu-id="fd13c-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="fd13c-112">表現</span><span class="sxs-lookup"><span data-stu-id="fd13c-112">Manifestation</span></span>

<span data-ttu-id="fd13c-113">我們找不到這種新行為的負面影響;不過，您應該要注意，因為它可能會導致媒體寫入軟體發生非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="fd13c-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="fd13c-114">降低</span><span class="sxs-lookup"><span data-stu-id="fd13c-114">Mitigation</span></span>

<span data-ttu-id="fd13c-115">若要還原為 alwayson 狀態，請關閉登錄中的這項功能。</span><span class="sxs-lookup"><span data-stu-id="fd13c-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="fd13c-116">登錄值的絕對路徑為：</span><span class="sxs-lookup"><span data-stu-id="fd13c-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="fd13c-117">其類型為 DWORD (32 位) ，如果其值為0，則 ZPODD 會停用;如果是任何其他值，則會啟用 ZPODD。</span><span class="sxs-lookup"><span data-stu-id="fd13c-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="fd13c-118">測試</span><span class="sxs-lookup"><span data-stu-id="fd13c-118">Tests</span></span>

<span data-ttu-id="fd13c-119">測試您的媒體撰寫軟體是否有因這項新功能而發生的任何異常狀況。</span><span class="sxs-lookup"><span data-stu-id="fd13c-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="fd13c-120">請 [通知 Microsoft](mailto:OptIssue@microsoft.com) 您使用這項新功能時所發現的任何問題。</span><span class="sxs-lookup"><span data-stu-id="fd13c-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




