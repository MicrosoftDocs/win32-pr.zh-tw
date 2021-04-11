---
title: 'RB_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與 Rebar 控制項相關聯之任何工具提示控制項的控制碼。
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104436"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="01957-104">RB \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="01957-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="01957-105">抓取與 Rebar 控制項相關聯之任何工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="01957-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01957-106">參數</span><span class="sxs-lookup"><span data-stu-id="01957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01957-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01957-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="01957-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="01957-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="01957-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01957-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="01957-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="01957-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01957-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="01957-111">Return value</span></span>

<span data-ttu-id="01957-112">傳回 **HWND** 值，此值是與 Rebar 控制項相關聯之工具提示控制項的控制碼; 如果沒有工具提示控制項與 Rebar 控制項相關聯，則為零。</span><span class="sxs-lookup"><span data-stu-id="01957-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="01957-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="01957-113">Requirements</span></span>



| <span data-ttu-id="01957-114">需求</span><span class="sxs-lookup"><span data-stu-id="01957-114">Requirement</span></span> | <span data-ttu-id="01957-115">值</span><span class="sxs-lookup"><span data-stu-id="01957-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01957-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01957-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01957-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01957-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01957-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01957-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01957-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01957-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01957-120">標頭</span><span class="sxs-lookup"><span data-stu-id="01957-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01957-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="01957-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





