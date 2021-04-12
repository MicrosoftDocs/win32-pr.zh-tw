---
title: 'CB_GETCOMBOBOXINFO 訊息 (Winuser .h) '
description: 取得指定下拉式方塊的相關資訊。
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464436"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="3c3a1-104">CB \_ GETCOMBOBOXINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="3c3a1-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="3c3a1-105">取得指定下拉式方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c3a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c3a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c3a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a1-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3c3a1-109">*lParam* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c3a1-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3a1-110">接收資訊之 [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3a1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c3a1-111">Return value</span></span>

<span data-ttu-id="3c3a1-112">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="3c3a1-113">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="3c3a1-114">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3a1-115">備註</span><span class="sxs-lookup"><span data-stu-id="3c3a1-115">Remarks</span></span>

<span data-ttu-id="3c3a1-116">此訊息相當於 [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)。</span><span class="sxs-lookup"><span data-stu-id="3c3a1-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3a1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c3a1-117">Requirements</span></span>



| <span data-ttu-id="3c3a1-118">需求</span><span class="sxs-lookup"><span data-stu-id="3c3a1-118">Requirement</span></span> | <span data-ttu-id="3c3a1-119">值</span><span class="sxs-lookup"><span data-stu-id="3c3a1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3a1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c3a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3a1-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c3a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c3a1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c3a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3a1-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c3a1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c3a1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3c3a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c3a1-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3c3a1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3a1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c3a1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c3a1-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="3c3a1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c3a1-128">**COMBOBOXINFO**</span><span class="sxs-lookup"><span data-stu-id="3c3a1-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="3c3a1-129">**GetComboBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="3c3a1-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

