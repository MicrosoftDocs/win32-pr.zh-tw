---
title: 'TB_GETITEMDROPDOWNRECT 訊息 (Commctrl .h) '
description: 取得具有樣式 BTNS 下拉式清單的工具列專案之下拉式視窗的周框 \_ 。
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024719"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="89896-104">TB \_ GETITEMDROPDOWNRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="89896-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="89896-105">取得具有樣式 [**BTNS \_ 下拉式清單**](toolbar-control-and-button-styles.md)的工具列專案之下拉式視窗的周框。</span><span class="sxs-lookup"><span data-stu-id="89896-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="89896-106">參數</span><span class="sxs-lookup"><span data-stu-id="89896-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89896-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89896-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89896-108">要抓取周框的工具列控制項專案之以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="89896-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="89896-109">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="89896-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="89896-110"><a href="/previous-versions//dd162897(v=vs.85)">**矩形**</a>結構的指標，用來接收周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="89896-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="89896-111">訊息寄件者負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="89896-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="89896-112">在 **矩形** 結構中傳回的座標會以用戶端座標表示。</span><span class="sxs-lookup"><span data-stu-id="89896-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89896-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="89896-113">Return value</span></span>

<span data-ttu-id="89896-114">一律傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="89896-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="89896-115">備註</span><span class="sxs-lookup"><span data-stu-id="89896-115">Remarks</span></span>

<span data-ttu-id="89896-116">專案必須具有 [ [**BTNS \_ ] 下拉式清單**](toolbar-control-and-button-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="89896-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="89896-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="89896-117">Requirements</span></span>



| <span data-ttu-id="89896-118">需求</span><span class="sxs-lookup"><span data-stu-id="89896-118">Requirement</span></span> | <span data-ttu-id="89896-119">值</span><span class="sxs-lookup"><span data-stu-id="89896-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89896-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89896-120">Minimum supported client</span></span><br/> | <span data-ttu-id="89896-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89896-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89896-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89896-122">Minimum supported server</span></span><br/> | <span data-ttu-id="89896-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89896-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89896-124">標頭</span><span class="sxs-lookup"><span data-stu-id="89896-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="89896-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="89896-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

