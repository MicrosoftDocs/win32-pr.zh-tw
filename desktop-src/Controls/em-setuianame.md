---
title: 'EM_SETUIANAME 訊息 (Richedit .h) '
description: 針對消費者介面自動化 (UIA) 設定 rich edit 控制項的名稱。
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934542"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="4648f-104">EM \_ SETUIANAME 訊息</span><span class="sxs-lookup"><span data-stu-id="4648f-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="4648f-105">針對消費者介面自動化 (UIA) 設定 rich edit 控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4648f-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="4648f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4648f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4648f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4648f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4648f-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="4648f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4648f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4648f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4648f-110">以 null 結束之名稱字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4648f-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4648f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4648f-111">Return value</span></span>

<span data-ttu-id="4648f-112">如果成功設定 UIA 的名稱，則為 TRUE，否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="4648f-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4648f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4648f-113">Requirements</span></span>



| <span data-ttu-id="4648f-114">需求</span><span class="sxs-lookup"><span data-stu-id="4648f-114">Requirement</span></span> | <span data-ttu-id="4648f-115">值</span><span class="sxs-lookup"><span data-stu-id="4648f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4648f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4648f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4648f-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4648f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4648f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4648f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4648f-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4648f-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4648f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4648f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4648f-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4648f-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





