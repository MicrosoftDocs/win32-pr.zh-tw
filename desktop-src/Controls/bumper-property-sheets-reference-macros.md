---
title: 屬性工作表宏
description: 屬性工作表宏
ms.assetid: d1cb44ec-b130-413a-8763-5997a2362b21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4986544551685002d21abd3fec06033bbc4628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106990007"
---
# <a name="property-sheet-macros"></a><span data-ttu-id="081e9-103">屬性工作表宏</span><span class="sxs-lookup"><span data-stu-id="081e9-103">Property Sheet Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="081e9-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="081e9-104">In This Section</span></span>

-   [<span data-ttu-id="081e9-105">**PropSheet \_ AddPage**</span><span class="sxs-lookup"><span data-stu-id="081e9-105">**PropSheet\_AddPage**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)
-   [<span data-ttu-id="081e9-106">**PropSheet \_ Apply**</span><span class="sxs-lookup"><span data-stu-id="081e9-106">**PropSheet\_Apply**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply)
-   [<span data-ttu-id="081e9-107">**PropSheet \_ CancelToClose**</span><span class="sxs-lookup"><span data-stu-id="081e9-107">**PropSheet\_CancelToClose**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose)
-   [<span data-ttu-id="081e9-108">**PropSheet \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="081e9-108">**PropSheet\_Changed**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed)
-   [<span data-ttu-id="081e9-109">**PropSheet \_ EnableWizButtons**</span><span class="sxs-lookup"><span data-stu-id="081e9-109">**PropSheet\_EnableWizButtons**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)
-   [<span data-ttu-id="081e9-110">**PropSheet \_ GetCurrentPageHwnd**</span><span class="sxs-lookup"><span data-stu-id="081e9-110">**PropSheet\_GetCurrentPageHwnd**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd)
-   [<span data-ttu-id="081e9-111">**PropSheet \_ GetResult**</span><span class="sxs-lookup"><span data-stu-id="081e9-111">**PropSheet\_GetResult**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)
-   [<span data-ttu-id="081e9-112">**PropSheet \_ GetTabControl**</span><span class="sxs-lookup"><span data-stu-id="081e9-112">**PropSheet\_GetTabControl**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)
-   [<span data-ttu-id="081e9-113">**PropSheet \_ HwndToIndex**</span><span class="sxs-lookup"><span data-stu-id="081e9-113">**PropSheet\_HwndToIndex**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex)
-   [<span data-ttu-id="081e9-114">**PropSheet \_ IdToIndex**</span><span class="sxs-lookup"><span data-stu-id="081e9-114">**PropSheet\_IdToIndex**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex)
-   [<span data-ttu-id="081e9-115">**PropSheet \_ IndexToHwnd**</span><span class="sxs-lookup"><span data-stu-id="081e9-115">**PropSheet\_IndexToHwnd**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd)
-   [<span data-ttu-id="081e9-116">**PropSheet \_ IndexToId**</span><span class="sxs-lookup"><span data-stu-id="081e9-116">**PropSheet\_IndexToId**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid)
-   [<span data-ttu-id="081e9-117">**PropSheet \_ IndexToPage**</span><span class="sxs-lookup"><span data-stu-id="081e9-117">**PropSheet\_IndexToPage**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage)
-   [<span data-ttu-id="081e9-118">**PropSheet \_ InsertPage**</span><span class="sxs-lookup"><span data-stu-id="081e9-118">**PropSheet\_InsertPage**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage)
-   [<span data-ttu-id="081e9-119">**PropSheet \_ IsDialogMessage**</span><span class="sxs-lookup"><span data-stu-id="081e9-119">**PropSheet\_IsDialogMessage**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)
-   [<span data-ttu-id="081e9-120">**PropSheet \_ PageToIndex**</span><span class="sxs-lookup"><span data-stu-id="081e9-120">**PropSheet\_PageToIndex**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex)
-   [<span data-ttu-id="081e9-121">**PropSheet \_ PressButton**</span><span class="sxs-lookup"><span data-stu-id="081e9-121">**PropSheet\_PressButton**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton)
-   [<span data-ttu-id="081e9-122">**PropSheet \_ QuerySiblings**</span><span class="sxs-lookup"><span data-stu-id="081e9-122">**PropSheet\_QuerySiblings**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)
-   [<span data-ttu-id="081e9-123">**PropSheet \_ RebootSystem**</span><span class="sxs-lookup"><span data-stu-id="081e9-123">**PropSheet\_RebootSystem**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem)
-   [<span data-ttu-id="081e9-124">**PropSheet \_ RecalcPageSizes**</span><span class="sxs-lookup"><span data-stu-id="081e9-124">**PropSheet\_RecalcPageSizes**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes)
-   [<span data-ttu-id="081e9-125">**PropSheet \_ RemovePage**</span><span class="sxs-lookup"><span data-stu-id="081e9-125">**PropSheet\_RemovePage**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)
-   [<span data-ttu-id="081e9-126">**PropSheet \_ RestartWindows**</span><span class="sxs-lookup"><span data-stu-id="081e9-126">**PropSheet\_RestartWindows**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows)
-   [<span data-ttu-id="081e9-127">**PropSheet \_ SetButtonText**</span><span class="sxs-lookup"><span data-stu-id="081e9-127">**PropSheet\_SetButtonText**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)
-   [<span data-ttu-id="081e9-128">**PropSheet \_ SetCurSel**</span><span class="sxs-lookup"><span data-stu-id="081e9-128">**PropSheet\_SetCurSel**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel)
-   [<span data-ttu-id="081e9-129">**PropSheet \_ SetCurSelByID**</span><span class="sxs-lookup"><span data-stu-id="081e9-129">**PropSheet\_SetCurSelByID**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid)
-   [<span data-ttu-id="081e9-130">**PropSheet \_ SetFinishText**</span><span class="sxs-lookup"><span data-stu-id="081e9-130">**PropSheet\_SetFinishText**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)
-   <span data-ttu-id="081e9-131">[**PropSheet \_ SetHeaderBitmap**](/previous-versions/windows/desktop/legacy/bb760787(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="081e9-131">[**PropSheet\_SetHeaderBitmap**](/previous-versions/windows/desktop/legacy/bb760787(v=vs.85))</span></span>
-   <span data-ttu-id="081e9-132">[**PropSheet \_ SetHeaderBitmapResource**](/previous-versions/windows/desktop/legacy/bb760789(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="081e9-132">[**PropSheet\_SetHeaderBitmapResource**](/previous-versions/windows/desktop/legacy/bb760789(v=vs.85))</span></span>
-   [<span data-ttu-id="081e9-133">**PropSheet \_ SetHeaderSubTitle**</span><span class="sxs-lookup"><span data-stu-id="081e9-133">**PropSheet\_SetHeaderSubTitle**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle)
-   [<span data-ttu-id="081e9-134">**PropSheet \_ SetHeaderTitle**</span><span class="sxs-lookup"><span data-stu-id="081e9-134">**PropSheet\_SetHeaderTitle**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle)
-   [<span data-ttu-id="081e9-135">**PropSheet \_ SetNextText**</span><span class="sxs-lookup"><span data-stu-id="081e9-135">**PropSheet\_SetNextText**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)
-   [<span data-ttu-id="081e9-136">**PropSheet \_ SetTitle**</span><span class="sxs-lookup"><span data-stu-id="081e9-136">**PropSheet\_SetTitle**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)
-   [<span data-ttu-id="081e9-137">**PropSheet \_ SetWizButtons**</span><span class="sxs-lookup"><span data-stu-id="081e9-137">**PropSheet\_SetWizButtons**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons)
-   [<span data-ttu-id="081e9-138">**PropSheet \_ ShowWizButtons**</span><span class="sxs-lookup"><span data-stu-id="081e9-138">**PropSheet\_ShowWizButtons**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons)
-   [<span data-ttu-id="081e9-139">**PropSheet \_ 未變更**</span><span class="sxs-lookup"><span data-stu-id="081e9-139">**PropSheet\_UnChanged**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged)

 

 
