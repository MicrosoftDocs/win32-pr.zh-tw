---
description: Windows Server 2003 （含 Service Pack 1）的二進位檔 (SP1) 與 Windows Vista 和 Windows Server 2008 相容。 不過，必須重新編譯舊版 Windows 的二進位檔。
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: 移植備份應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513133"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="58fcb-104">移植備份應用程式</span><span class="sxs-lookup"><span data-stu-id="58fcb-104">Porting Backup Applications</span></span>

<span data-ttu-id="58fcb-105">Windows Server 2003 （含 Service Pack 1）的二進位檔 (SP1) 與 Windows Vista 和 Windows Server 2008 相容。</span><span class="sxs-lookup"><span data-stu-id="58fcb-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="58fcb-106">不過，必須重新編譯舊版 Windows 的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="58fcb-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="58fcb-107">將 Windows XP 備份應用程式移植到 Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58fcb-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="58fcb-108">自 Windows XP 起，有數個 VSS 介面已經變更。</span><span class="sxs-lookup"><span data-stu-id="58fcb-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="58fcb-109">Windows XP 應用程式至少必須使用來自 VSS 7.2 SDK 或 Windows Vista 或 Windows Server 2008 SDK 的標頭檔和程式庫重新編譯。</span><span class="sxs-lookup"><span data-stu-id="58fcb-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="58fcb-110">將 Windows Server 2003 SP1 備份應用程式移植到 Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58fcb-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="58fcb-111">Windows Server 2003 （含 SP1）中的二進位檔與 Windows Vista 和 Windows Server 2008 相容。</span><span class="sxs-lookup"><span data-stu-id="58fcb-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="58fcb-112">不過，大部分的 Windows Server 2003 SP1 備份應用程式都必須更新，以考慮新功能，如下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="58fcb-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="58fcb-113">編譯適用于 Windows Vista 的備份應用程式</span><span class="sxs-lookup"><span data-stu-id="58fcb-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="58fcb-114">您可以使用 VSS 7.2 SDK 中提供的標頭檔和程式庫，來編譯使用 Windows Server 2003 中可用介面的應用程式。</span><span class="sxs-lookup"><span data-stu-id="58fcb-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="58fcb-115">若要使用新的介面，必須使用 Windows Vista SDK 隨附的標頭檔和程式庫重新編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="58fcb-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="58fcb-116">使用 Windows Vista 或 Windows Server 2008 編譯的二進位檔與 Windows Server 2003 SP1 或舊版 Windows 不相容。</span><span class="sxs-lookup"><span data-stu-id="58fcb-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



