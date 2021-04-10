---
title: 'HDM_GETORDERARRAY 訊息 (Commctrl .h) '
description: 取得標題控制項中專案的目前由左到右的順序。 您可以明確地傳送此訊息，或使用標頭 \_ GetOrderArray 宏。
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103770"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="8b443-105">HDM \_ GETORDERARRAY 訊息</span><span class="sxs-lookup"><span data-stu-id="8b443-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="8b443-106">取得標題控制項中專案的目前由左到右的順序。</span><span class="sxs-lookup"><span data-stu-id="8b443-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="8b443-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) 宏。</span><span class="sxs-lookup"><span data-stu-id="8b443-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b443-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b443-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b443-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b443-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b443-110">*LParam* 可保存的整數元素數目。</span><span class="sxs-lookup"><span data-stu-id="8b443-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="8b443-111">這個值必須等於控制項中的專案數 (請參閱 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8b443-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b443-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b443-113">整數陣列的指標，可接收標頭中專案的索引值。</span><span class="sxs-lookup"><span data-stu-id="8b443-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b443-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b443-114">Return value</span></span>

<span data-ttu-id="8b443-115">如果成功，則會傳回非零，而 *lParam* 的緩衝區會接收標題控制項中每個專案的專案編號（依其出現的順序，由左至右排列）。</span><span class="sxs-lookup"><span data-stu-id="8b443-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="8b443-116">否則，訊息會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8b443-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b443-117">備註</span><span class="sxs-lookup"><span data-stu-id="8b443-117">Remarks</span></span>

<span data-ttu-id="8b443-118">*LParam* 中的元素數目是在 *wParam* 中指定，而且必須等於控制項中的專案數。</span><span class="sxs-lookup"><span data-stu-id="8b443-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="8b443-119">例如，下列程式碼片段會保留足夠的記憶體來保存索引值。</span><span class="sxs-lookup"><span data-stu-id="8b443-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="8b443-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b443-120">Requirements</span></span>



| <span data-ttu-id="8b443-121">需求</span><span class="sxs-lookup"><span data-stu-id="8b443-121">Requirement</span></span> | <span data-ttu-id="8b443-122">值</span><span class="sxs-lookup"><span data-stu-id="8b443-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b443-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b443-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b443-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b443-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b443-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b443-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b443-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b443-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b443-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8b443-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b443-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





