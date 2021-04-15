---
title: 'WM_COPYDATA 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ COPYDATA 訊息，以將資料傳遞給另一個應用程式。
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA 訊息資料交換
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465616"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="3243e-104">WM \_ COPYDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="3243e-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="3243e-105">應用程式會傳送 **WM \_ COPYDATA** 訊息，以將資料傳遞給另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="3243e-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="3243e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3243e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3243e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3243e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3243e-108">傳遞資料的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="3243e-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="3243e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3243e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3243e-110">[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)結構的指標，其中包含要傳遞的資料。</span><span class="sxs-lookup"><span data-stu-id="3243e-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3243e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3243e-111">Return value</span></span>

<span data-ttu-id="3243e-112">如果接收的應用程式處理此訊息，它應該會傳回 **TRUE**;否則，它應該會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3243e-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3243e-113">備註</span><span class="sxs-lookup"><span data-stu-id="3243e-113">Remarks</span></span>

<span data-ttu-id="3243e-114">傳遞的資料不能包含指標或其他物件參考，無法存取接收資料的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3243e-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="3243e-115">傳送此訊息時，所參考的資料不得由傳送進程的另一個執行緒變更。</span><span class="sxs-lookup"><span data-stu-id="3243e-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="3243e-116">接收應用程式應該將資料視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="3243e-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="3243e-117">*LParam* 參數只在訊息處理期間有效。</span><span class="sxs-lookup"><span data-stu-id="3243e-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="3243e-118">接收的應用程式不應該釋放 *lParam* 所參考的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3243e-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="3243e-119">如果接收應用程式必須在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回之後存取資料，則必須將資料複製到本機緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3243e-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="3243e-120">範例</span><span class="sxs-lookup"><span data-stu-id="3243e-120">Examples</span></span>

<span data-ttu-id="3243e-121">如需範例，請參閱 [使用資料複製](using-data-copy.md)。</span><span class="sxs-lookup"><span data-stu-id="3243e-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3243e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3243e-122">Requirements</span></span>



| <span data-ttu-id="3243e-123">需求</span><span class="sxs-lookup"><span data-stu-id="3243e-123">Requirement</span></span> | <span data-ttu-id="3243e-124">值</span><span class="sxs-lookup"><span data-stu-id="3243e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3243e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3243e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3243e-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3243e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3243e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3243e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3243e-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3243e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3243e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3243e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3243e-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3243e-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3243e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3243e-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="3243e-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="3243e-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3243e-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="3243e-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="3243e-134">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3243e-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

