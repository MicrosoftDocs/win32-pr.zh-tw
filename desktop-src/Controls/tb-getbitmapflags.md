---
title: 'TB_GETBITMAPFLAGS 訊息 (Commctrl .h) '
description: 抓取描述要使用之點陣圖類型的旗標。
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106602"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="0b1c8-104">TB \_ GETBITMAPFLAGS 訊息</span><span class="sxs-lookup"><span data-stu-id="0b1c8-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="0b1c8-105">抓取描述要使用之點陣圖類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b1c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b1c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b1c8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b1c8-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0b1c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b1c8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0b1c8-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1c8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b1c8-111">Return value</span></span>

<span data-ttu-id="0b1c8-112">傳回 **DWORD** 值，描述應該使用的點陣圖類型。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="0b1c8-113">如果此傳回值已設定 TBBF \_ 大型旗標，則應用程式應該使用大型點陣圖 (24 x 24) ; 否則，應用程式應該使用小型點陣圖 (16 x 16) 。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="0b1c8-114">所有其他位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1c8-115">備註</span><span class="sxs-lookup"><span data-stu-id="0b1c8-115">Remarks</span></span>

<span data-ttu-id="0b1c8-116">**TB \_ GETBITMAPFLAGS** 所傳回的值只是諮詢。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="0b1c8-117">工具列控制項會根據使用者選擇的是大型或小型字型來建議大型或小型點陣圖。</span><span class="sxs-lookup"><span data-stu-id="0b1c8-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1c8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b1c8-118">Requirements</span></span>



| <span data-ttu-id="0b1c8-119">需求</span><span class="sxs-lookup"><span data-stu-id="0b1c8-119">Requirement</span></span> | <span data-ttu-id="0b1c8-120">值</span><span class="sxs-lookup"><span data-stu-id="0b1c8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1c8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b1c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1c8-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b1c8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b1c8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b1c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1c8-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b1c8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b1c8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0b1c8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1c8-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1c8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





