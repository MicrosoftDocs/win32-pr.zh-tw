---
title: 'TB_HASACCELERATOR 訊息 (Commctrl .h) '
description: 抓取具有指定快速鍵的工具列按鈕計數。
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR message Windows 控制項
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465565"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="79742-104">TB \_ HASACCELERATOR 訊息</span><span class="sxs-lookup"><span data-stu-id="79742-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="79742-105">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="79742-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="79742-106">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="79742-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="79742-107">抓取具有指定快速鍵的工具列按鈕計數。</span><span class="sxs-lookup"><span data-stu-id="79742-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="79742-108">參數</span><span class="sxs-lookup"><span data-stu-id="79742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79742-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79742-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79742-110">**WCHAR** ，表示要測試的輸入快速鍵字元。</span><span class="sxs-lookup"><span data-stu-id="79742-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="79742-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79742-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79742-112">整數的指標，該 **int** 會接收具有快速鍵字元的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="79742-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79742-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="79742-113">Return value</span></span>

<span data-ttu-id="79742-114">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="79742-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="79742-115">安全性考量</span><span class="sxs-lookup"><span data-stu-id="79742-115">Security Considerations</span></span>

<span data-ttu-id="79742-116">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="79742-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="79742-117">備註</span><span class="sxs-lookup"><span data-stu-id="79742-117">Remarks</span></span>

<span data-ttu-id="79742-118">首先，系統會查詢所有工具列按鈕，以進行相符的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="79742-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="79742-119">如果找不到相符專案，系統會將 [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) 通知傳送至父視窗，要求具有指定快速鍵的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="79742-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="79742-120">如果父系提供索引，則計數會設定為1。</span><span class="sxs-lookup"><span data-stu-id="79742-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="79742-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="79742-121">Requirements</span></span>



| <span data-ttu-id="79742-122">需求</span><span class="sxs-lookup"><span data-stu-id="79742-122">Requirement</span></span> | <span data-ttu-id="79742-123">值</span><span class="sxs-lookup"><span data-stu-id="79742-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79742-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79742-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79742-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79742-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79742-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79742-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79742-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79742-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79742-128">標頭</span><span class="sxs-lookup"><span data-stu-id="79742-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79742-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="79742-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





