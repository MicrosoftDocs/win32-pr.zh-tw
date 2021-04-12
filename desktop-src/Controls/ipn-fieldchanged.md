---
title: 'IPN_FIELDCHANGED (Commctrl 的通知碼) '
description: 當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025343"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="890ca-105">IPN \_ FIELDCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="890ca-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="890ca-106">當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。</span><span class="sxs-lookup"><span data-stu-id="890ca-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="890ca-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="890ca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="890ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="890ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="890ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="890ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="890ca-110">[**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress)結構的指標，其中包含已變更之位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="890ca-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="890ca-111">此結構的 **iValue** 成員會包含輸入的值，即使超出欄位的範圍也一樣。</span><span class="sxs-lookup"><span data-stu-id="890ca-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="890ca-112">您可以將此成員修改為欄位範圍內的任何值，以回應此通知碼。</span><span class="sxs-lookup"><span data-stu-id="890ca-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="890ca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="890ca-113">Return value</span></span>

<span data-ttu-id="890ca-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="890ca-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="890ca-115">備註</span><span class="sxs-lookup"><span data-stu-id="890ca-115">Remarks</span></span>

<span data-ttu-id="890ca-116">此通知碼不會傳送以回應 [**IPM \_ SETADDRESS**](ipm-setaddress.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="890ca-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="890ca-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="890ca-117">Requirements</span></span>



| <span data-ttu-id="890ca-118">需求</span><span class="sxs-lookup"><span data-stu-id="890ca-118">Requirement</span></span> | <span data-ttu-id="890ca-119">值</span><span class="sxs-lookup"><span data-stu-id="890ca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="890ca-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="890ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="890ca-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="890ca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="890ca-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="890ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="890ca-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="890ca-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="890ca-124">標頭</span><span class="sxs-lookup"><span data-stu-id="890ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="890ca-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="890ca-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





