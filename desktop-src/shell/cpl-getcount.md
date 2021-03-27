---
description: 傳送至主控台應用程式的 CPlApplet 函式，以取得應用程式所支援的對話方塊數目。
title: 'CPL_GETCOUNT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511059"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="de3d1-103">CPL \_ GETCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="de3d1-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="de3d1-104">傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以取得應用程式所支援的對話方塊數目。</span><span class="sxs-lookup"><span data-stu-id="de3d1-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="de3d1-105">參數</span><span class="sxs-lookup"><span data-stu-id="de3d1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3d1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de3d1-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="de3d1-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="de3d1-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="de3d1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de3d1-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de3d1-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="de3d1-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3d1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="de3d1-110">Return value</span></span>

<span data-ttu-id="de3d1-111">[**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc)函式會傳回主控台應用程式所支援的對話方塊數目。</span><span class="sxs-lookup"><span data-stu-id="de3d1-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3d1-112">備註</span><span class="sxs-lookup"><span data-stu-id="de3d1-112">Remarks</span></span>

<span data-ttu-id="de3d1-113">這則訊息會緊接在 [**CPL \_ 初始**](cpl-init.md) 訊息之後傳送。</span><span class="sxs-lookup"><span data-stu-id="de3d1-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3d1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="de3d1-114">Requirements</span></span>



| <span data-ttu-id="de3d1-115">需求</span><span class="sxs-lookup"><span data-stu-id="de3d1-115">Requirement</span></span> | <span data-ttu-id="de3d1-116">值</span><span class="sxs-lookup"><span data-stu-id="de3d1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de3d1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de3d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de3d1-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de3d1-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="de3d1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de3d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de3d1-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de3d1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="de3d1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="de3d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3d1-122"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="de3d1-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
