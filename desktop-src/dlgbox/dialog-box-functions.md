---
title: 對話方塊函式
description: 對話方塊函式
ms.assetid: 7ea6445a-1772-4986-b4b7-27512afa680d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44e63184a75a9bc3bddedc4f8c037719689fced
ms.sourcegitcommit: 57e91b10658c36e28dd8ebe3e77d5b9bec4fbcc2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/15/2021
ms.locfileid: "107509837"
---
# <a name="dialog-box-functions"></a><span data-ttu-id="dbc60-103">對話方塊函式</span><span class="sxs-lookup"><span data-stu-id="dbc60-103">Dialog box functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dbc60-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="dbc60-104">In this section</span></span>

* [<span data-ttu-id="dbc60-105">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="dbc60-105">**CreateDialog**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialoga)
* [<span data-ttu-id="dbc60-106">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="dbc60-106">**CreateDialogIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogindirecta)
* [<span data-ttu-id="dbc60-107">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="dbc60-107">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogindirectparama)
* [<span data-ttu-id="dbc60-108">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="dbc60-108">**CreateDialogParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogparama)
* [<span data-ttu-id="dbc60-109">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="dbc60-109">**DefDlgProc**</span></span>](/windows/win32/api/Winuser/nf-winuser-defdlgprocw)
* [<span data-ttu-id="dbc60-110">**對話方塊**</span><span class="sxs-lookup"><span data-stu-id="dbc60-110">**DialogBox**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxa)
* [<span data-ttu-id="dbc60-111">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="dbc60-111">**DialogBoxIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxindirecta)
* [<span data-ttu-id="dbc60-112">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="dbc60-112">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxindirectparama)
* [<span data-ttu-id="dbc60-113">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="dbc60-113">**DialogBoxParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxparama)
* [<span data-ttu-id="dbc60-114">**DLGPROC**</span><span class="sxs-lookup"><span data-stu-id="dbc60-114">**DLGPROC**</span></span>](/windows/win32/api/winuser/nc-winuser-dlgproc)
* [<span data-ttu-id="dbc60-115">**EndDialog**</span><span class="sxs-lookup"><span data-stu-id="dbc60-115">**EndDialog**</span></span>](/windows/win32/api/Winuser/nf-winuser-enddialog)
* [<span data-ttu-id="dbc60-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="dbc60-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdialogbaseunits)
* [<span data-ttu-id="dbc60-117">**GetDlgCtrlID**</span><span class="sxs-lookup"><span data-stu-id="dbc60-117">**GetDlgCtrlID**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgctrlid)
* [<span data-ttu-id="dbc60-118">**GetDlgItem**</span><span class="sxs-lookup"><span data-stu-id="dbc60-118">**GetDlgItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitem)
* [<span data-ttu-id="dbc60-119">**GetDlgItemInt**</span><span class="sxs-lookup"><span data-stu-id="dbc60-119">**GetDlgItemInt**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitemint)
* [<span data-ttu-id="dbc60-120">**GetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="dbc60-120">**GetDlgItemText**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitemtexta)
* [<span data-ttu-id="dbc60-121">**GetNextDlgGroupItem**</span><span class="sxs-lookup"><span data-stu-id="dbc60-121">**GetNextDlgGroupItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getnextdlggroupitem)
* [<span data-ttu-id="dbc60-122">**GetNextDlgTabItem**</span><span class="sxs-lookup"><span data-stu-id="dbc60-122">**GetNextDlgTabItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getnextdlgtabitem)
* [<span data-ttu-id="dbc60-123">**IsDialogMessage**</span><span class="sxs-lookup"><span data-stu-id="dbc60-123">**IsDialogMessage**</span></span>](/windows/win32/api/Winuser/nf-winuser-isdialogmessagea)
* [<span data-ttu-id="dbc60-124">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="dbc60-124">**MapDialogRect**</span></span>](/windows/win32/api/Winuser/nf-winuser-mapdialogrect)
* [<span data-ttu-id="dbc60-125">**MessageBox**</span><span class="sxs-lookup"><span data-stu-id="dbc60-125">**MessageBox**</span></span>](/windows/win32/api/Winuser/nf-winuser-messagebox)
* [<span data-ttu-id="dbc60-126">**MessageBoxEx**</span><span class="sxs-lookup"><span data-stu-id="dbc60-126">**MessageBoxEx**</span></span>](/windows/win32/api/Winuser/nf-winuser-messageboxexa)
* [<span data-ttu-id="dbc60-127">**MessageBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="dbc60-127">**MessageBoxIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-messageboxindirecta)
* [<span data-ttu-id="dbc60-128">**MSGBOXCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="dbc60-128">**MSGBOXCALLBACK**</span></span>](/windows/win32/api/winuser/nc-winuser-msgboxcallback)
* [<span data-ttu-id="dbc60-129">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="dbc60-129">**SendDlgItemMessage**</span></span>](/windows/win32/api/Winuser/nf-winuser-senddlgitemmessagea)
* [<span data-ttu-id="dbc60-130">**SetDlgItemInt**</span><span class="sxs-lookup"><span data-stu-id="dbc60-130">**SetDlgItemInt**</span></span>](/windows/win32/api/Winuser/nf-winuser-setdlgitemint)
* [<span data-ttu-id="dbc60-131">**SetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="dbc60-131">**SetDlgItemText**</span></span>](/windows/win32/api/Winuser/nf-winuser-setdlgitemtexta)
