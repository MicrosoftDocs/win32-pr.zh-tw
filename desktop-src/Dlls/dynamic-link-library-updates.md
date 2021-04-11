---
description: 有時需要以較新的版本取代 DLL。
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link 程式庫更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f76103ddebc723466fb7e32a216c0c039691d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026385"
---
# <a name="dynamic-link-library-updates"></a><span data-ttu-id="7e96d-103">Dynamic-Link 程式庫更新</span><span class="sxs-lookup"><span data-stu-id="7e96d-103">Dynamic-Link Library Updates</span></span>

<span data-ttu-id="7e96d-104">有時需要以較新的版本取代 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-104">It is sometimes necessary to replace a DLL with a newer version.</span></span> <span data-ttu-id="7e96d-105">取代 DLL 之前，請先執行版本檢查，以確定您要以較新的版本取代舊版。</span><span class="sxs-lookup"><span data-stu-id="7e96d-105">Before replacing a DLL, perform a version check to ensure that you are replacing an older version with a newer version.</span></span> <span data-ttu-id="7e96d-106">您可以取代使用中的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-106">It is possible to replace a DLL that is in use.</span></span> <span data-ttu-id="7e96d-107">您用來取代使用中 Dll 的方法，取決於您所使用的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7e96d-107">The method you use to replace DLLs that are in use depends on the operating system you are using.</span></span> <span data-ttu-id="7e96d-108">在 Windows XP 和更新版本中，應用程式應該使用 [隔離的應用程式和並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。</span><span class="sxs-lookup"><span data-stu-id="7e96d-108">On Windows XP and later, applications should use [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="7e96d-109">如果您執行下列步驟，就不需要重新開機電腦：</span><span class="sxs-lookup"><span data-stu-id="7e96d-109">It is not necessary to restart the computer if you perform the following steps:</span></span>

1.  <span data-ttu-id="7e96d-110">使用 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) 函式來重新命名要取代的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-110">Use the [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) function to rename the DLL being replaced.</span></span> <span data-ttu-id="7e96d-111">請勿指定 \_ \_ 允許的 MOVEFILE 複製，並確認重新命名的檔案位於包含原始檔案的相同磁片區上。</span><span class="sxs-lookup"><span data-stu-id="7e96d-111">Do not specify MOVEFILE\_COPY\_ALLOWED, and make sure the renamed file is on the same volume that contains the original file.</span></span> <span data-ttu-id="7e96d-112">您也可以將檔案命名為不同的擴充功能，以在相同的目錄中重新命名該檔案。</span><span class="sxs-lookup"><span data-stu-id="7e96d-112">You could also simply rename the file in the same directory by giving it a different extension.</span></span>
2.  <span data-ttu-id="7e96d-113">將新的 DLL 複製到包含已重新命名之 DLL 的目錄。</span><span class="sxs-lookup"><span data-stu-id="7e96d-113">Copy the new DLL to the directory that contains the renamed DLL.</span></span> <span data-ttu-id="7e96d-114">所有應用程式現在會使用新的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-114">All applications will now use the new DLL.</span></span>
3.  <span data-ttu-id="7e96d-115">使用 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) 搭配 MOVEFILE \_ 延遲 \_ 直到 \_ 重新開機，以刪除重新命名的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-115">Use [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) with MOVEFILE\_DELAY\_UNTIL\_REBOOT to delete the renamed DLL.</span></span>

<span data-ttu-id="7e96d-116">在您進行這項取代之前，應用程式將會使用原始 DLL，直到卸載為止。</span><span class="sxs-lookup"><span data-stu-id="7e96d-116">Before you make this replacement, applications will use the original DLL until it is unloaded.</span></span> <span data-ttu-id="7e96d-117">在您進行取代之後，應用程式將會使用新的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-117">After you make the replacement, applications will use the new DLL.</span></span> <span data-ttu-id="7e96d-118">當您撰寫 DLL 時，您必須小心確認它已準備好用於這種情況，特別是當 DLL 維持全域狀態資訊或與其他服務通訊時。</span><span class="sxs-lookup"><span data-stu-id="7e96d-118">When you write a DLL, you must be careful to ensure that it is prepared for this situation, especially if the DLL maintains global state information or communicates with other services.</span></span> <span data-ttu-id="7e96d-119">如果 DLL 未針對全域狀態資訊或通訊協定的變更做好準備，更新 DLL 將會要求您重新開機電腦，以確保所有應用程式都使用相同版本的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7e96d-119">If the DLL is not prepared for a change in global state information or communication protocols, updating the DLL will require you to restart the computer to ensure that all applications are using the same version of the DLL.</span></span>

 

 
