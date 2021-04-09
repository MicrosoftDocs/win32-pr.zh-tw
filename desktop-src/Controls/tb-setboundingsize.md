---
title: 'TB_SETBOUNDINGSIZE 訊息 (Commctrl .h) '
description: 設定多欄工具列控制項的周框大小。
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843056"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="4a508-104">TB \_ SETBOUNDINGSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="4a508-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="4a508-105">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="4a508-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="4a508-106">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="4a508-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="4a508-107">設定多欄工具列控制項的周框大小。</span><span class="sxs-lookup"><span data-stu-id="4a508-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a508-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a508-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a508-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a508-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a508-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4a508-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a508-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a508-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a508-112">[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，其 **cy** 成員包含周框高度。</span><span class="sxs-lookup"><span data-stu-id="4a508-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="4a508-113">會忽略 (寬度) 的 **cx** 成員。</span><span class="sxs-lookup"><span data-stu-id="4a508-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a508-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a508-114">Return value</span></span>

<span data-ttu-id="4a508-115">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="4a508-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="4a508-116">安全性考量</span><span class="sxs-lookup"><span data-stu-id="4a508-116">Security Considerations</span></span>

<span data-ttu-id="4a508-117">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="4a508-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a508-118">備註</span><span class="sxs-lookup"><span data-stu-id="4a508-118">Remarks</span></span>

<span data-ttu-id="4a508-119">周框大小可控制如何將按鈕組織成資料行。</span><span class="sxs-lookup"><span data-stu-id="4a508-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="4a508-120">如果工具列控制項沒有 TBSTYLE EX 的多重 [**\_ \_ 列**](toolbar-extended-styles.md) 樣式，則此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="4a508-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a508-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a508-121">Requirements</span></span>



| <span data-ttu-id="4a508-122">需求</span><span class="sxs-lookup"><span data-stu-id="4a508-122">Requirement</span></span> | <span data-ttu-id="4a508-123">值</span><span class="sxs-lookup"><span data-stu-id="4a508-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a508-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a508-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a508-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a508-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a508-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a508-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a508-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a508-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a508-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4a508-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a508-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a508-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

