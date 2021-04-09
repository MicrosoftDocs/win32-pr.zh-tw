---
title: 'LB_GETLISTBOXINFO 訊息 (Winuser .h) '
description: 取得指定清單方塊中每個資料行的專案數。
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- LB_GETLISTBOXINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024993"
---
# <a name="lb_getlistboxinfo-message"></a><span data-ttu-id="60f74-104">LB \_ GETLISTBOXINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="60f74-104">LB\_GETLISTBOXINFO message</span></span>

<span data-ttu-id="60f74-105">取得指定清單方塊中每個資料行的專案數。</span><span class="sxs-lookup"><span data-stu-id="60f74-105">Gets the number of items per column in a specified list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="60f74-106">參數</span><span class="sxs-lookup"><span data-stu-id="60f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f74-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60f74-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60f74-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="60f74-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="60f74-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60f74-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60f74-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="60f74-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f74-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="60f74-111">Return value</span></span>

<span data-ttu-id="60f74-112">傳回值是每個資料行的專案數。</span><span class="sxs-lookup"><span data-stu-id="60f74-112">The return value is the number of items per column.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f74-113">備註</span><span class="sxs-lookup"><span data-stu-id="60f74-113">Remarks</span></span>

<span data-ttu-id="60f74-114">此訊息相當於 [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)。</span><span class="sxs-lookup"><span data-stu-id="60f74-114">This message is equivalent to [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="60f74-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="60f74-115">Requirements</span></span>



| <span data-ttu-id="60f74-116">需求</span><span class="sxs-lookup"><span data-stu-id="60f74-116">Requirement</span></span> | <span data-ttu-id="60f74-117">值</span><span class="sxs-lookup"><span data-stu-id="60f74-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f74-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60f74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60f74-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60f74-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60f74-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60f74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60f74-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60f74-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60f74-122">標頭</span><span class="sxs-lookup"><span data-stu-id="60f74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60f74-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="60f74-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f74-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60f74-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f74-125">**GetListBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="60f74-125">**GetListBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





