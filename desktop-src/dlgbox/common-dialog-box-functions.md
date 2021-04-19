---
title: 通用對話方塊函數
description: . |通用對話方塊函數
ms.assetid: 4a94330b-e0d5-48d7-80f3-86ba6ca1f0f9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f0ca24f319bb27955ba117a8035df3042fb44
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993848"
---
# <a name="common-dialog-box-functions"></a><span data-ttu-id="5ef46-104">通用對話方塊函數</span><span class="sxs-lookup"><span data-stu-id="5ef46-104">Common Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ef46-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="5ef46-105">In this section</span></span>

-   [<span data-ttu-id="5ef46-106">*CCHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-106">*CCHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)
-   [<span data-ttu-id="5ef46-107">*CFHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-107">*CFHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
-   <span data-ttu-id="5ef46-108">[**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ef46-108">[**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span></span>
-   [<span data-ttu-id="5ef46-109">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="5ef46-109">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="5ef46-110">**CommDlgExtendedError**</span><span class="sxs-lookup"><span data-stu-id="5ef46-110">**CommDlgExtendedError**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror)
-   [<span data-ttu-id="5ef46-111">**FindText**</span><span class="sxs-lookup"><span data-stu-id="5ef46-111">**FindText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)
-   [<span data-ttu-id="5ef46-112">*FRHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-112">*FRHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)
-   [<span data-ttu-id="5ef46-113">**GetFileTitle**</span><span class="sxs-lookup"><span data-stu-id="5ef46-113">**GetFileTitle**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)
-   [<span data-ttu-id="5ef46-114">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="5ef46-114">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
-   [<span data-ttu-id="5ef46-115">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5ef46-115">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
-   [<span data-ttu-id="5ef46-116">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-116">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
-   <span data-ttu-id="5ef46-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ef46-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span></span>
-   [<span data-ttu-id="5ef46-118">**PagePaintHook**</span><span class="sxs-lookup"><span data-stu-id="5ef46-118">**PagePaintHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
-   <span data-ttu-id="5ef46-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ef46-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
-   [<span data-ttu-id="5ef46-120">**PageSetupHook**</span><span class="sxs-lookup"><span data-stu-id="5ef46-120">**PageSetupHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)
-   <span data-ttu-id="5ef46-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ef46-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span></span>
-   <span data-ttu-id="5ef46-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ef46-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span></span>
-   [<span data-ttu-id="5ef46-123">*PrintHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-123">*PrintHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)
-   [<span data-ttu-id="5ef46-124">**Replacer.replacetext**</span><span class="sxs-lookup"><span data-stu-id="5ef46-124">**ReplaceText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)
-   [<span data-ttu-id="5ef46-125">*SetupHookProc*</span><span class="sxs-lookup"><span data-stu-id="5ef46-125">*SetupHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)

 

 
