---
description: 當使用者按兩下應用程式所支援之對話方塊的圖示時，傳送至主控台應用程式的 CPlApplet 函式。
title: 'CPL_DBLCLK 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991086"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="0a4ef-103">CPL \_ DBLCLK 訊息</span><span class="sxs-lookup"><span data-stu-id="0a4ef-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="0a4ef-104">當使用者按兩下應用程式所支援之對話方塊的圖示時，傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a4ef-105">參數</span><span class="sxs-lookup"><span data-stu-id="0a4ef-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4ef-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="0a4ef-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="0a4ef-107">對話方塊編號。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-107">The dialog box number.</span></span> <span data-ttu-id="0a4ef-108">此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="0a4ef-109">*lData*</span><span class="sxs-lookup"><span data-stu-id="0a4ef-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="0a4ef-110">主控台應用程式載入至對話方塊之 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的 **lpData** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="0a4ef-111">應用程式會載入 **lpData** 成員，以回應 [**CPL \_ INQUIRE**](cpl-inquire.md) 或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4ef-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a4ef-112">Return value</span></span>

<span data-ttu-id="0a4ef-113">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則傳回值為零。否則，則為非零。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4ef-114">備註</span><span class="sxs-lookup"><span data-stu-id="0a4ef-114">Remarks</span></span>

<span data-ttu-id="0a4ef-115">為了回應此訊息，主控台的應用程式必須顯示對應的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0a4ef-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4ef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a4ef-116">Requirements</span></span>



| <span data-ttu-id="0a4ef-117">需求</span><span class="sxs-lookup"><span data-stu-id="0a4ef-117">Requirement</span></span> | <span data-ttu-id="0a4ef-118">值</span><span class="sxs-lookup"><span data-stu-id="0a4ef-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0a4ef-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a4ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4ef-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a4ef-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0a4ef-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a4ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4ef-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a4ef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a4ef-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0a4ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a4ef-124"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ef-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4ef-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a4ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ef-126">**CPL \_ 選取**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
