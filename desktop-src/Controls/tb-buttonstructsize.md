---
title: 'TB_BUTTONSTRUCTSIZE 訊息 (Commctrl .h) '
description: 指定 TBBUTTON 結構的大小。
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025503"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="a61bf-104">TB \_ BUTTONSTRUCTSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a61bf-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="a61bf-105">指定 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="a61bf-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="a61bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="a61bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a61bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a61bf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a61bf-108">[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a61bf-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a61bf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a61bf-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a61bf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a61bf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a61bf-111">Return value</span></span>

<span data-ttu-id="a61bf-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a61bf-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a61bf-113">備註</span><span class="sxs-lookup"><span data-stu-id="a61bf-113">Remarks</span></span>

<span data-ttu-id="a61bf-114">系統會使用大小來判斷所使用的通用控制項動態連結程式庫 () 版本。</span><span class="sxs-lookup"><span data-stu-id="a61bf-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="a61bf-115">如果應用程式使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立工具列，則應用程式必須在傳送 [**TB \_ ADDBITMAP**](tb-addbitmap.md) 或 [**tb \_ ADDBUTTONS**](tb-addbuttons.md) 訊息之前，將此訊息傳送至工具列。</span><span class="sxs-lookup"><span data-stu-id="a61bf-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="a61bf-116">[**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)函式會自動傳送 **TB 的 \_ BUTTONSTRUCTSIZE**，而 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的大小是函數的參數。</span><span class="sxs-lookup"><span data-stu-id="a61bf-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a61bf-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a61bf-117">Requirements</span></span>



| <span data-ttu-id="a61bf-118">需求</span><span class="sxs-lookup"><span data-stu-id="a61bf-118">Requirement</span></span> | <span data-ttu-id="a61bf-119">值</span><span class="sxs-lookup"><span data-stu-id="a61bf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a61bf-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a61bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a61bf-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a61bf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a61bf-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a61bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a61bf-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a61bf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a61bf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a61bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a61bf-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a61bf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

