---
title: 'TTM_GETCURRENTTOOL 訊息 (Commctrl .h) '
description: 抓取工具提示控制項中目前工具的資訊。
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934398"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="979f0-104">TTM \_ GETCURRENTTOOL 訊息</span><span class="sxs-lookup"><span data-stu-id="979f0-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="979f0-105">抓取工具提示控制項中目前工具的資訊。</span><span class="sxs-lookup"><span data-stu-id="979f0-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="979f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="979f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="979f0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="979f0-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="979f0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="979f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="979f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="979f0-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會接收目前工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="979f0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="979f0-111">如果這個值為 **Null**，則傳回值會指出目前的工具是否存在，而不會實際抓取工具資訊。</span><span class="sxs-lookup"><span data-stu-id="979f0-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="979f0-112">如果這個值不是 **Null**，則必須先填入 **TOOLINFO** 結構的 **cbSize** 成員，才能傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="979f0-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979f0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="979f0-113">Return value</span></span>

<span data-ttu-id="979f0-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="979f0-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="979f0-115">如果 *lParam* 為 **Null**，則傳回非零值（如果目前的工具存在），否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="979f0-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="979f0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="979f0-116">Requirements</span></span>



| <span data-ttu-id="979f0-117">需求</span><span class="sxs-lookup"><span data-stu-id="979f0-117">Requirement</span></span> | <span data-ttu-id="979f0-118">值</span><span class="sxs-lookup"><span data-stu-id="979f0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="979f0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="979f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="979f0-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="979f0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="979f0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="979f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="979f0-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="979f0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="979f0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="979f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="979f0-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="979f0-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="979f0-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="979f0-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="979f0-126">**TTM \_GETCURRENTTOOLW** (Unicode) 和 **TTM \_ GETCURRENTTOOLA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="979f0-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





