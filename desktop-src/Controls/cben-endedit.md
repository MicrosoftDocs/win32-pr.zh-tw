---
title: 'CBEN_ENDEDIT (Commctrl 的通知碼) '
description: 當使用者在編輯方塊內結束作業，或已從控制項下拉式清單中選取專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383934"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="54cac-105">CBEN \_ ENDEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="54cac-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="54cac-106">當使用者在編輯方塊內結束作業，或已從控制項下拉式清單中選取專案時傳送。</span><span class="sxs-lookup"><span data-stu-id="54cac-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="54cac-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="54cac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="54cac-108">參數</span><span class="sxs-lookup"><span data-stu-id="54cac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54cac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54cac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54cac-110">[**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)結構的指標，其中包含使用者如何結束編輯作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="54cac-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54cac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="54cac-111">Return value</span></span>

<span data-ttu-id="54cac-112">**FALSE** 表示接受通知碼，並允許控制項顯示選取的專案;否則 **為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="54cac-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cac-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="54cac-113">Requirements</span></span>



| <span data-ttu-id="54cac-114">需求</span><span class="sxs-lookup"><span data-stu-id="54cac-114">Requirement</span></span> | <span data-ttu-id="54cac-115">值</span><span class="sxs-lookup"><span data-stu-id="54cac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54cac-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54cac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54cac-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54cac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54cac-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54cac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54cac-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54cac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54cac-120">標頭</span><span class="sxs-lookup"><span data-stu-id="54cac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="54cac-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54cac-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="54cac-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="54cac-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54cac-123">**CBEN \_ENDEDITW** (Unicode) 和 **CBEN \_ ENDEDITA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="54cac-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="54cac-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54cac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cac-125">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="54cac-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 





