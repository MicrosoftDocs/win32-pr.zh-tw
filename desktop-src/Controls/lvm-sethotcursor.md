---
title: 'LVM_SETHOTCURSOR 訊息 (Commctrl .h) '
description: 設定當啟用熱追蹤時，清單視圖控制項所使用的 HCURSOR 值。
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685519"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="dc085-104">LVM \_ SETHOTCURSOR 訊息</span><span class="sxs-lookup"><span data-stu-id="dc085-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="dc085-105">設定當啟用熱追蹤時，清單視圖控制項所使用的 HCURSOR 值。</span><span class="sxs-lookup"><span data-stu-id="dc085-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="dc085-106">您可以明確地傳送此訊息，或使用 [**ListView \_ SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) 宏。</span><span class="sxs-lookup"><span data-stu-id="dc085-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="dc085-107">若要檢查是否已啟用熱追蹤，請呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。</span><span class="sxs-lookup"><span data-stu-id="dc085-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="dc085-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc085-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc085-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc085-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc085-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="dc085-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc085-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc085-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc085-112">要設定之資料指標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dc085-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc085-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc085-113">Return value</span></span>

<span data-ttu-id="dc085-114">傳回 HCURSOR 值，此值為先前的熱資料指標。</span><span class="sxs-lookup"><span data-stu-id="dc085-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc085-115">備註</span><span class="sxs-lookup"><span data-stu-id="dc085-115">Remarks</span></span>

<span data-ttu-id="dc085-116">當設定 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 樣式時，清單視圖控制項會使用熱追蹤和暫留選取專案。</span><span class="sxs-lookup"><span data-stu-id="dc085-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc085-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc085-117">Requirements</span></span>



| <span data-ttu-id="dc085-118">需求</span><span class="sxs-lookup"><span data-stu-id="dc085-118">Requirement</span></span> | <span data-ttu-id="dc085-119">值</span><span class="sxs-lookup"><span data-stu-id="dc085-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc085-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc085-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc085-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc085-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc085-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc085-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc085-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc085-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc085-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dc085-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc085-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc085-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

