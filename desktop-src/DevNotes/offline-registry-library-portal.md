---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: 離線登錄庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972123"
---
# <a name="offline-registry-library"></a><span data-ttu-id="33bb7-103">離線登錄庫</span><span class="sxs-lookup"><span data-stu-id="33bb7-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="33bb7-104">目的</span><span class="sxs-lookup"><span data-stu-id="33bb7-104">Purpose</span></span>

<span data-ttu-id="33bb7-105">離線登錄庫 (Offreg.dll) 用來修改作用中系統登錄之外的登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="33bb7-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="33bb7-106">此程式庫適用于登錄更新案例，例如服務作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="33bb7-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="33bb7-107">從 Windows Vista 開始，程式庫支援登錄 hive 格式。</span><span class="sxs-lookup"><span data-stu-id="33bb7-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="33bb7-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="33bb7-108">Developer audience</span></span>

<span data-ttu-id="33bb7-109">這項技術適用于原始設備製造商 (Oem) 、防毒軟體和反惡意程式碼軟體廠商，以及必須能夠剖析登錄 hive 檔案的其他應用程式開發人員，而不需要將它們載入 active registry。</span><span class="sxs-lookup"><span data-stu-id="33bb7-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="33bb7-110">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="33bb7-110">Run-time requirements</span></span>

<span data-ttu-id="33bb7-111">離線登錄庫會以二進位可轉散發的動態連結程式庫的形式提供， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="33bb7-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="33bb7-112">此程式庫會在下列版本的 Windows 上執行：</span><span class="sxs-lookup"><span data-stu-id="33bb7-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="33bb7-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="33bb7-113">Windows Server 2016</span></span>  
<span data-ttu-id="33bb7-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="33bb7-114">Windows 10</span></span>  
<span data-ttu-id="33bb7-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33bb7-115">Windows 8.1</span></span>  
<span data-ttu-id="33bb7-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33bb7-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="33bb7-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="33bb7-117">Windows 8</span></span>  
<span data-ttu-id="33bb7-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33bb7-118">Windows Server 2012</span></span>  
<span data-ttu-id="33bb7-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33bb7-119">Windows 7</span></span>  
<span data-ttu-id="33bb7-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33bb7-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="33bb7-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33bb7-121">Windows Server 2008</span></span>  
<span data-ttu-id="33bb7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33bb7-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="33bb7-123">應用程式應該使用動態連結連結至 Offreg.dll。</span><span class="sxs-lookup"><span data-stu-id="33bb7-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="33bb7-124">Offreg.dll 是在適用于 Windows 10 和較早版本 Windows 作業系統的 Windows 驅動程式套件 (WDK) 中提供。</span><span class="sxs-lookup"><span data-stu-id="33bb7-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="33bb7-125">如需取得 WDK 的詳細資訊，請參閱 [如何取得 wdk 和 WLK](/windows-hardware/drivers/download-the-wdk) 或造訪 [MSDN 訂閱](https://msdn.microsoft.com/subscriptions/default.aspx) 網站。</span><span class="sxs-lookup"><span data-stu-id="33bb7-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="33bb7-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="33bb7-126">In this section</span></span>

-   [<span data-ttu-id="33bb7-127">**關於離線登錄庫**</span><span class="sxs-lookup"><span data-stu-id="33bb7-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="33bb7-128">**離線登錄庫函數**</span><span class="sxs-lookup"><span data-stu-id="33bb7-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
