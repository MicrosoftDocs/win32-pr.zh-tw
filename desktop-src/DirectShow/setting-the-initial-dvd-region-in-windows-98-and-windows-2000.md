---
description: 設定初始 DVD 區域
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: 設定初始 DVD 區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509758"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="d06c4-103">設定初始 DVD 區域</span><span class="sxs-lookup"><span data-stu-id="d06c4-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="d06c4-104">系統製造商必須在電腦上選取 DVD 光碟機的初始 DVD 區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="d06c4-105">只有加密的光碟可以用來設定區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="d06c4-106">Windows 2000 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d06c4-106">Windows 2000 and Later</span></span>

<span data-ttu-id="d06c4-107">從 Windows 2000 開始，預設的 DVD 區域會根據設定電腦的地區設定來選取。</span><span class="sxs-lookup"><span data-stu-id="d06c4-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="d06c4-108">如果磁片磁碟機中有光碟片，Windows 2000 一律會使用此預設區域以及光碟區域來設定 DVD 光碟機的初始區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="d06c4-109">系統製造商不需要執行任何動作來設定 Windows 2000 或更新版本 DVD 磁片磁碟機的初始區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="d06c4-110">針對 RPC1 磁片磁碟機，如果開機時磁片磁碟機中沒有光碟片，則預設區域只會根據電腦的地區設定來設定。</span><span class="sxs-lookup"><span data-stu-id="d06c4-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="d06c4-111">在開機時，如果磁片磁碟機中有 DVD 光碟，則會選取預設區域作為磁片磁碟機的區域，前提是它符合光碟的區域;否則，光碟上的最社區域會挑選為磁片磁碟機的初始區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="d06c4-112">如果預設值不正確，使用者 (或系統製造商) 會允許一項剩餘的變更。</span><span class="sxs-lookup"><span data-stu-id="d06c4-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="d06c4-113">針對 RPC2 磁片磁碟機，如果在安裝過程中，Windows 2000 發現磁片磁碟機沒有設定任何區域，則會嘗試挑選上面的區域，但只有在磁片磁碟機中有光碟時。</span><span class="sxs-lookup"><span data-stu-id="d06c4-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="d06c4-114"> (RPC1 磁片磁碟機會選擇沒有任何磁片磁碟機) 的區域。</span><span class="sxs-lookup"><span data-stu-id="d06c4-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="d06c4-115">設定 RPC2 磁片磁碟機的區域之後，重新安裝或全新的作業系統安裝並不會自動變更。</span><span class="sxs-lookup"><span data-stu-id="d06c4-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="d06c4-116">OEM 可以設定包含系統預設 DVD 區域的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d06c4-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="d06c4-117">第一次開機時，磁片磁碟機區域會設定為此值。</span><span class="sxs-lookup"><span data-stu-id="d06c4-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="d06c4-118">Windows 2000 和更新版本上的登錄機碼為 HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (binary) 。</span><span class="sxs-lookup"><span data-stu-id="d06c4-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="d06c4-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d06c4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06c4-120">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="d06c4-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



