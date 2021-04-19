---
description: 抓取控制項目前用來繪製其文字的字型。
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: 'WM_GETFONT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994394"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="c4af0-103">WM \_ GETFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="c4af0-103">WM\_GETFONT message</span></span>

<span data-ttu-id="c4af0-104">抓取控制項目前用來繪製其文字的字型。</span><span class="sxs-lookup"><span data-stu-id="c4af0-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="c4af0-105">參數</span><span class="sxs-lookup"><span data-stu-id="c4af0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4af0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4af0-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4af0-107">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="c4af0-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4af0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4af0-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4af0-109">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="c4af0-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4af0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4af0-110">Return value</span></span>

<span data-ttu-id="c4af0-111">類型： **HFONT**</span><span class="sxs-lookup"><span data-stu-id="c4af0-111">Type: **HFONT**</span></span>

<span data-ttu-id="c4af0-112">傳回值是控制項所使用之字型的控制碼; 如果控制項使用系統字型，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c4af0-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4af0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4af0-113">Requirements</span></span>



| <span data-ttu-id="c4af0-114">需求</span><span class="sxs-lookup"><span data-stu-id="c4af0-114">Requirement</span></span> | <span data-ttu-id="c4af0-115">值</span><span class="sxs-lookup"><span data-stu-id="c4af0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4af0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4af0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4af0-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4af0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c4af0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4af0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4af0-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4af0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4af0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c4af0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4af0-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c4af0-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4af0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4af0-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4af0-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="c4af0-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4af0-124">**WM \_ SETFONT**</span><span class="sxs-lookup"><span data-stu-id="c4af0-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="c4af0-125">**概念**</span><span class="sxs-lookup"><span data-stu-id="c4af0-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4af0-126">Windows</span><span class="sxs-lookup"><span data-stu-id="c4af0-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




