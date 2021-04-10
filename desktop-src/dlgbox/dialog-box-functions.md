---
title: 對話方塊函式
description: .
ms.assetid: 7ea6445a-1772-4986-b4b7-27512afa680d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 789e450e0a6e42157f0036f5d1e805856fcc8b95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024063"
---
# <a name="dialog-box-functions"></a><span data-ttu-id="7342d-103">對話方塊函式</span><span class="sxs-lookup"><span data-stu-id="7342d-103">Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7342d-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="7342d-104">In this section</span></span>

-   [<span data-ttu-id="7342d-105">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="7342d-105">**CreateDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialoga)
-   [<span data-ttu-id="7342d-106">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="7342d-106">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="7342d-107">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="7342d-107">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="7342d-108">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="7342d-108">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
-   [<span data-ttu-id="7342d-109">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="7342d-109">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
-   [<span data-ttu-id="7342d-110">**對話方塊**</span><span class="sxs-lookup"><span data-stu-id="7342d-110">**DialogBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxa)
-   [<span data-ttu-id="7342d-111">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="7342d-111">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="7342d-112">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="7342d-112">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
-   [<span data-ttu-id="7342d-113">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="7342d-113">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
-   [<span data-ttu-id="7342d-114">*DialogProc*</span><span class="sxs-lookup"><span data-stu-id="7342d-114">*DialogProc*</span></span>](/windows/win32/api/winuser/nc-winuser-dlgproc)
-   [<span data-ttu-id="7342d-115">**EndDialog**</span><span class="sxs-lookup"><span data-stu-id="7342d-115">**EndDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enddialog)
-   [<span data-ttu-id="7342d-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="7342d-116">**GetDialogBaseUnits**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits)
-   [<span data-ttu-id="7342d-117">**GetDlgCtrlID**</span><span class="sxs-lookup"><span data-stu-id="7342d-117">**GetDlgCtrlID**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)
-   [<span data-ttu-id="7342d-118">**GetDlgItem**</span><span class="sxs-lookup"><span data-stu-id="7342d-118">**GetDlgItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)
-   [<span data-ttu-id="7342d-119">**GetDlgItemInt**</span><span class="sxs-lookup"><span data-stu-id="7342d-119">**GetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint)
-   [<span data-ttu-id="7342d-120">**GetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="7342d-120">**GetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta)
-   [<span data-ttu-id="7342d-121">**GetNextDlgGroupItem**</span><span class="sxs-lookup"><span data-stu-id="7342d-121">**GetNextDlgGroupItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem)
-   [<span data-ttu-id="7342d-122">**GetNextDlgTabItem**</span><span class="sxs-lookup"><span data-stu-id="7342d-122">**GetNextDlgTabItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem)
-   [<span data-ttu-id="7342d-123">**IsDialogMessage**</span><span class="sxs-lookup"><span data-stu-id="7342d-123">**IsDialogMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea)
-   [<span data-ttu-id="7342d-124">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="7342d-124">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
-   [<span data-ttu-id="7342d-125">**MessageBox**</span><span class="sxs-lookup"><span data-stu-id="7342d-125">**MessageBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messagebox)
-   [<span data-ttu-id="7342d-126">**MessageBoxEx**</span><span class="sxs-lookup"><span data-stu-id="7342d-126">**MessageBoxEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)
-   [<span data-ttu-id="7342d-127">**MessageBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="7342d-127">**MessageBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxindirecta)
-   [<span data-ttu-id="7342d-128">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="7342d-128">**SendDlgItemMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea)
-   [<span data-ttu-id="7342d-129">**SetDlgItemInt**</span><span class="sxs-lookup"><span data-stu-id="7342d-129">**SetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint)
-   [<span data-ttu-id="7342d-130">**SetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="7342d-130">**SetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta)

 

 