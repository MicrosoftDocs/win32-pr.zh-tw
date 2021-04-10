---
title: 'HDN_DROPDOWN (Commctrl 的通知碼) '
description: 當按一下標題控制項上的下拉箭號時，由標題控制項傳送至其父代。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844488"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="62d5a-105">HDN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="62d5a-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="62d5a-106">當按一下標題控制項上的下拉箭號時，由標題控制項傳送至其父代。</span><span class="sxs-lookup"><span data-stu-id="62d5a-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="62d5a-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="62d5a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="62d5a-108">參數</span><span class="sxs-lookup"><span data-stu-id="62d5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62d5a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62d5a-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的資訊。</span><span class="sxs-lookup"><span data-stu-id="62d5a-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d5a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62d5a-111">Return value</span></span>

<span data-ttu-id="62d5a-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="62d5a-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d5a-113">備註</span><span class="sxs-lookup"><span data-stu-id="62d5a-113">Remarks</span></span>

<span data-ttu-id="62d5a-114">「語法」一節中的範例會顯示通知接收者如何轉換 **LPARAM** 以取得 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構。</span><span class="sxs-lookup"><span data-stu-id="62d5a-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="62d5a-115">**WPARAM** 包含傳送此訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="62d5a-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="62d5a-116">只有在 \_ 標題專案上設定 STYLE HDF SPLITBUTTON 時，才會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="62d5a-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="62d5a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="62d5a-117">Requirements</span></span>



| <span data-ttu-id="62d5a-118">需求</span><span class="sxs-lookup"><span data-stu-id="62d5a-118">Requirement</span></span> | <span data-ttu-id="62d5a-119">值</span><span class="sxs-lookup"><span data-stu-id="62d5a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62d5a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62d5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62d5a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62d5a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62d5a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62d5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62d5a-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62d5a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62d5a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="62d5a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62d5a-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="62d5a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





