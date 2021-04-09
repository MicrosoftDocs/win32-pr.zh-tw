---
title: 'TB_ADDBITMAP 訊息 (Commctrl .h) '
description: 將一或多個影像新增至適用于工具列的按鈕影像清單。
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686663"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="a766b-104">TB \_ ADDBITMAP 訊息</span><span class="sxs-lookup"><span data-stu-id="a766b-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="a766b-105">將一或多個影像新增至適用于工具列的按鈕影像清單。</span><span class="sxs-lookup"><span data-stu-id="a766b-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a766b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a766b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a766b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a766b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a766b-108">點陣圖中的按鈕影像數目。</span><span class="sxs-lookup"><span data-stu-id="a766b-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="a766b-109">如果 *lParam* 指定系統定義的點陣圖，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="a766b-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a766b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a766b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a766b-111">[**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)結構的指標，其中包含點陣圖資源的識別碼，以及包含點陣圖資源之可執行檔的模組實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="a766b-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a766b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a766b-112">Return value</span></span>

<span data-ttu-id="a766b-113">如果成功，則傳回第一個新影像的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="a766b-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a766b-114">備註</span><span class="sxs-lookup"><span data-stu-id="a766b-114">Remarks</span></span>

<span data-ttu-id="a766b-115">如果工具列是使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式所建立，您必須先將 [**tb \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) 訊息傳送至工具列，然後再傳送 **tb \_ ADDBITMAP**。</span><span class="sxs-lookup"><span data-stu-id="a766b-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="a766b-116">範例</span><span class="sxs-lookup"><span data-stu-id="a766b-116">Examples</span></span>

<span data-ttu-id="a766b-117">下列範例會從資源建立點陣圖 (.IDB \_ BITMAP1) 、在此) 案例中，將背景色彩對應 (黑色，然後將其新增至工具列。</span><span class="sxs-lookup"><span data-stu-id="a766b-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="a766b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a766b-118">Requirements</span></span>



| <span data-ttu-id="a766b-119">需求</span><span class="sxs-lookup"><span data-stu-id="a766b-119">Requirement</span></span> | <span data-ttu-id="a766b-120">值</span><span class="sxs-lookup"><span data-stu-id="a766b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a766b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a766b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a766b-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a766b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a766b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a766b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a766b-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a766b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a766b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a766b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a766b-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a766b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

