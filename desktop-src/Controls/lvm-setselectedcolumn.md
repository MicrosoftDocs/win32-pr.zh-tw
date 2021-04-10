---
title: 'LVM_SETSELECTEDCOLUMN 訊息 (Commctrl .h) '
description: 設定所選取資料行的索引。
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844487"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="12388-104">LVM \_ SETSELECTEDCOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="12388-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="12388-105">設定所選取資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="12388-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="12388-106">參數</span><span class="sxs-lookup"><span data-stu-id="12388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12388-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12388-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12388-108">指定資料行索引的 **int** 類型值。</span><span class="sxs-lookup"><span data-stu-id="12388-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="12388-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12388-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="12388-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="12388-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12388-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="12388-111">Return value</span></span>

<span data-ttu-id="12388-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="12388-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="12388-113">備註</span><span class="sxs-lookup"><span data-stu-id="12388-113">Remarks</span></span>

<span data-ttu-id="12388-114">資料行索引會儲存在 **int** 陣列中。</span><span class="sxs-lookup"><span data-stu-id="12388-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="12388-115">請參閱 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)的 **puColumns** 成員。</span><span class="sxs-lookup"><span data-stu-id="12388-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="12388-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="12388-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="12388-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="12388-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12388-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="12388-118">Requirements</span></span>



| <span data-ttu-id="12388-119">需求</span><span class="sxs-lookup"><span data-stu-id="12388-119">Requirement</span></span> | <span data-ttu-id="12388-120">值</span><span class="sxs-lookup"><span data-stu-id="12388-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12388-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12388-121">Minimum supported client</span></span><br/> | <span data-ttu-id="12388-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12388-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12388-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12388-123">Minimum supported server</span></span><br/> | <span data-ttu-id="12388-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12388-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12388-125">標頭</span><span class="sxs-lookup"><span data-stu-id="12388-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="12388-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="12388-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





