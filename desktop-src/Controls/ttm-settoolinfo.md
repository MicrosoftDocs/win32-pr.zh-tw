---
title: 'TTM_SETTOOLINFO 訊息 (Commctrl .h) '
description: 設定工具提示控制項為工具維護的資訊。
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466797"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="62156-104">TTM \_ SETTOOLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="62156-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="62156-105">設定工具提示控制項為工具維護的資訊。</span><span class="sxs-lookup"><span data-stu-id="62156-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="62156-106">參數</span><span class="sxs-lookup"><span data-stu-id="62156-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62156-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62156-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62156-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="62156-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62156-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62156-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62156-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，指定要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="62156-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="62156-111">傳送此訊息之前，必須先設定此結構的 **cbSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="62156-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62156-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="62156-112">Return value</span></span>

<span data-ttu-id="62156-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="62156-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62156-114">備註</span><span class="sxs-lookup"><span data-stu-id="62156-114">Remarks</span></span>

<span data-ttu-id="62156-115">工具的某些內部屬性會在建立工具時建立，而且在傳送 **TTM \_ SETTOOLINFO** 訊息時不會重新計算。</span><span class="sxs-lookup"><span data-stu-id="62156-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="62156-116">如果您只是將值指派給 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構，並將其傳遞至具有 **TTM \_ SETTOOLINFO** 訊息的工具提示控制項，這些屬性可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="62156-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="62156-117">相反地，您的應用程式應該先傳送工具提示控制項 a [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)訊息，以要求工具目前的 **TOOLINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="62156-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="62156-118">然後，視需要修改此結構的成員，並將其傳遞回具有 **TTM \_ SETTOOLINFO** 的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="62156-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="62156-119">呼叫 **TTM \_ SETTOOLINFO** 時， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **lpszText** 成員所指向的字串不得超過 80 **TCHARs** 的長度，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="62156-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62156-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="62156-120">Requirements</span></span>



| <span data-ttu-id="62156-121">需求</span><span class="sxs-lookup"><span data-stu-id="62156-121">Requirement</span></span> | <span data-ttu-id="62156-122">值</span><span class="sxs-lookup"><span data-stu-id="62156-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62156-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62156-123">Minimum supported client</span></span><br/> | <span data-ttu-id="62156-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62156-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62156-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62156-125">Minimum supported server</span></span><br/> | <span data-ttu-id="62156-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62156-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62156-127">標頭</span><span class="sxs-lookup"><span data-stu-id="62156-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="62156-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="62156-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="62156-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="62156-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="62156-130">**TTM \_SETTOOLINFOW** (Unicode) 和 **TTM \_ SETTOOLINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="62156-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





