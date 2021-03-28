---
description: 當控制項或功能表建立時，傳送至控制項或功能表項目的擁有者視窗。
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: 'DFM_WM_MEASUREITEM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386113"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="a225f-103">DFM \_ WM \_ MEASUREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="a225f-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="a225f-104">當控制項或功能表建立時，傳送至控制項或功能表項目的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="a225f-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="a225f-105">參數</span><span class="sxs-lookup"><span data-stu-id="a225f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a225f-106">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a225f-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a225f-107">*LpMeasureItem* 參數所指向之 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的 **CtlID** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="a225f-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="a225f-108">此值會識別傳送 **DFM \_ WM \_ MEASUREITEM** 訊息的控制項。</span><span class="sxs-lookup"><span data-stu-id="a225f-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="a225f-109">*lpMeasureItem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a225f-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a225f-110">[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的指標，其中包含主控描繪控制項或功能表項目的維度。</span><span class="sxs-lookup"><span data-stu-id="a225f-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a225f-111">備註</span><span class="sxs-lookup"><span data-stu-id="a225f-111">Remarks</span></span>

<span data-ttu-id="a225f-112">當擁有者視窗收到 **DFM 的 \_ WM \_ MEASUREITEM** 訊息時，擁有者會填入訊息的 *LpMeasureItem* 參數所指向的 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構並傳回; 這會通知系統有控制項的維度。</span><span class="sxs-lookup"><span data-stu-id="a225f-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a225f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a225f-113">Requirements</span></span>



| <span data-ttu-id="a225f-114">需求</span><span class="sxs-lookup"><span data-stu-id="a225f-114">Requirement</span></span> | <span data-ttu-id="a225f-115">值</span><span class="sxs-lookup"><span data-stu-id="a225f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a225f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a225f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a225f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a225f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a225f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a225f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a225f-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a225f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a225f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a225f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a225f-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="a225f-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
