---
title: 剪貼簿函數
description: . |剪貼簿函數
ms.assetid: 54addf54-921d-4246-b21e-ae993f8bcb02
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a6a0304c55e4c97f2243599909decd997758e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196023"
---
# <a name="clipboard-functions"></a><span data-ttu-id="edebd-104">剪貼簿函數</span><span class="sxs-lookup"><span data-stu-id="edebd-104">Clipboard Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="edebd-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="edebd-105">In this section</span></span>

-   [<span data-ttu-id="edebd-106">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="edebd-106">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
-   [<span data-ttu-id="edebd-107">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="edebd-107">**ChangeClipboardChain**</span></span>](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain)
-   [<span data-ttu-id="edebd-108">**CloseClipboard**</span><span class="sxs-lookup"><span data-stu-id="edebd-108">**CloseClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)
-   [<span data-ttu-id="edebd-109">**CountClipboardFormats**</span><span class="sxs-lookup"><span data-stu-id="edebd-109">**CountClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats)
-   [<span data-ttu-id="edebd-110">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="edebd-110">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
-   [<span data-ttu-id="edebd-111">**EnumClipboardFormats**</span><span class="sxs-lookup"><span data-stu-id="edebd-111">**EnumClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats)
-   [<span data-ttu-id="edebd-112">**GetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="edebd-112">**GetClipboardData**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata)
-   [<span data-ttu-id="edebd-113">**GetClipboardFormatName**</span><span class="sxs-lookup"><span data-stu-id="edebd-113">**GetClipboardFormatName**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)
-   [<span data-ttu-id="edebd-114">**GetClipboardOwner**</span><span class="sxs-lookup"><span data-stu-id="edebd-114">**GetClipboardOwner**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardowner)
-   [<span data-ttu-id="edebd-115">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="edebd-115">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
-   [<span data-ttu-id="edebd-116">**GetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="edebd-116">**GetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer)
-   [<span data-ttu-id="edebd-117">**GetOpenClipboardWindow**</span><span class="sxs-lookup"><span data-stu-id="edebd-117">**GetOpenClipboardWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow)
-   [<span data-ttu-id="edebd-118">**GetPriorityClipboardFormat**</span><span class="sxs-lookup"><span data-stu-id="edebd-118">**GetPriorityClipboardFormat**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat)
-   [<span data-ttu-id="edebd-119">**GetUpdatedClipboardFormats**</span><span class="sxs-lookup"><span data-stu-id="edebd-119">**GetUpdatedClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdatedclipboardformats)
-   [<span data-ttu-id="edebd-120">**IsClipboardFormatAvailable**</span><span class="sxs-lookup"><span data-stu-id="edebd-120">**IsClipboardFormatAvailable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)
-   [<span data-ttu-id="edebd-121">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="edebd-121">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
-   [<span data-ttu-id="edebd-122">**RegisterClipboardFormat**</span><span class="sxs-lookup"><span data-stu-id="edebd-122">**RegisterClipboardFormat**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)
-   [<span data-ttu-id="edebd-123">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="edebd-123">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
-   [<span data-ttu-id="edebd-124">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="edebd-124">**SetClipboardData**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata)
-   [<span data-ttu-id="edebd-125">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="edebd-125">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

 

 




