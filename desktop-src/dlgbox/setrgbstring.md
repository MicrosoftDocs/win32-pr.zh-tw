---
title: 'SETRGBSTRING message (Commdlg) '
description: '[色彩] 對話方塊（CCHookProc）的 [攔截程式] 可以將已註冊的 SETRGBSTRING 訊息傳送至對話方塊，以設定目前的色彩選取範圍。'
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- SETRGBSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686179"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="6d690-104">SETRGBSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="6d690-104">SETRGBSTRING message</span></span>

<span data-ttu-id="6d690-105">[ **色彩** ] 對話方塊（ [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)）的 [攔截程式] 可以將已註冊的 **SETRGBSTRING** 訊息傳送至對話方塊，以設定目前的色彩選取範圍。</span><span class="sxs-lookup"><span data-stu-id="6d690-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="6d690-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d690-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d690-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d690-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d690-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="6d690-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6d690-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d690-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d690-110">要在 [ **色彩** ] 對話方塊中選取之色彩的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="6d690-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="6d690-111">您可以使用 [**rgb**](/windows/desktop/api/wingdi/nf-wingdi-rgb) 宏來指定 rgb 色彩值的紅色、綠色和藍色濃度。</span><span class="sxs-lookup"><span data-stu-id="6d690-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d690-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d690-112">Return value</span></span>

<span data-ttu-id="6d690-113">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6d690-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d690-114">備註</span><span class="sxs-lookup"><span data-stu-id="6d690-114">Remarks</span></span>

<span data-ttu-id="6d690-115">如果 *lParam* 符合其中一個基本色彩或16個自訂色彩之一，則對話方塊程式會選取該色彩。</span><span class="sxs-lookup"><span data-stu-id="6d690-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="6d690-116">對話方塊程式也會更新 [ **色彩** ] 對話方塊之 [自訂色彩] 延伸中的所有控制項（如果已開啟）。</span><span class="sxs-lookup"><span data-stu-id="6d690-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="6d690-117">如果 *lParam* 不符合基本或自訂色彩，則對話方塊程式不會變更目前的色彩選取範圍，但會更新自訂色彩控制項（如果看得到的話）。</span><span class="sxs-lookup"><span data-stu-id="6d690-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="6d690-118">範例</span><span class="sxs-lookup"><span data-stu-id="6d690-118">Examples</span></span>

<span data-ttu-id="6d690-119">下列範例程式碼會取得 **SETRGBSTRING** 訊息識別碼，然後將色彩選取範圍設定為藍色。</span><span class="sxs-lookup"><span data-stu-id="6d690-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="6d690-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d690-120">Requirements</span></span>



| <span data-ttu-id="6d690-121">需求</span><span class="sxs-lookup"><span data-stu-id="6d690-121">Requirement</span></span> | <span data-ttu-id="6d690-122">值</span><span class="sxs-lookup"><span data-stu-id="6d690-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d690-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d690-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d690-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d690-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6d690-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d690-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d690-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d690-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d690-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6d690-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d690-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6d690-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6d690-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6d690-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6d690-130">**SETRGBSTRINGW** (Unicode) 和 **SETRGBSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6d690-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="6d690-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d690-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d690-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="6d690-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d690-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="6d690-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="6d690-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="6d690-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="6d690-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6d690-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="6d690-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="6d690-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d690-137">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="6d690-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

