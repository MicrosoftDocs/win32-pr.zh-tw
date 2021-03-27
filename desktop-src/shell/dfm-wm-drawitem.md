---
description: 當控制項或功能表的視覺外觀變更時，傳送至主控描繪控制項或功能表的父視窗。
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: 'DFM_WM_DRAWITEM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972005"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="ec627-103">DFM \_ WM \_ DRAWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="ec627-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="ec627-104">當控制項或功能表的視覺外觀變更時，傳送至主控描繪控制項或功能表的父視窗。</span><span class="sxs-lookup"><span data-stu-id="ec627-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="ec627-105">參數</span><span class="sxs-lookup"><span data-stu-id="ec627-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec627-106">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec627-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec627-107">傳送 **DFM \_ WM \_ DRAWITEM** 訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec627-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="ec627-108">如果訊息是由功能表傳送，此參數為零。</span><span class="sxs-lookup"><span data-stu-id="ec627-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec627-109">*lpDrawItem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ec627-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec627-110">[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的指標，其中包含要繪製之專案的相關資訊，以及所需的繪圖類型。</span><span class="sxs-lookup"><span data-stu-id="ec627-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec627-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec627-111">Return value</span></span>

<span data-ttu-id="ec627-112">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ec627-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec627-113">備註</span><span class="sxs-lookup"><span data-stu-id="ec627-113">Remarks</span></span>

<span data-ttu-id="ec627-114">[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemAction** 成員會指定應用程式應該執行的繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="ec627-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="ec627-115">從處理此訊息傳回之前，應用程式應該確定 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **hDC** 成員所識別的裝置內容為預設狀態。</span><span class="sxs-lookup"><span data-stu-id="ec627-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec627-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec627-116">Requirements</span></span>



| <span data-ttu-id="ec627-117">需求</span><span class="sxs-lookup"><span data-stu-id="ec627-117">Requirement</span></span> | <span data-ttu-id="ec627-118">值</span><span class="sxs-lookup"><span data-stu-id="ec627-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec627-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec627-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ec627-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec627-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ec627-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec627-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ec627-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec627-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec627-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ec627-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec627-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec627-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
