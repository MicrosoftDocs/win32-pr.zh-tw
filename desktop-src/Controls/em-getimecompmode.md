---
title: 'EM_GETIMECOMPMODE 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項的目前輸入方法編輯器 (IME) 模式。
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466105"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="b0287-104">EM \_ GETIMECOMPMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="b0287-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="b0287-105">抓取 rich edit 控制項的目前輸入方法編輯器 (IME) 模式。</span><span class="sxs-lookup"><span data-stu-id="b0287-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0287-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0287-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0287-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0287-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b0287-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b0287-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0287-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0287-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b0287-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0287-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0287-111">Return value</span></span>

<span data-ttu-id="b0287-112">傳回值是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b0287-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="b0287-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b0287-113">Return code</span></span>                                                                                     | <span data-ttu-id="b0287-114">Description</span><span class="sxs-lookup"><span data-stu-id="b0287-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="b0287-115"><dt>**ICM \_ NOTOPEN**</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="b0287-116">未開啟 IME。</span><span class="sxs-lookup"><span data-stu-id="b0287-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="b0287-117"><dt>**ICM \_ 級別3**</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="b0287-118">True 內嵌模式。</span><span class="sxs-lookup"><span data-stu-id="b0287-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="b0287-119"><dt>**ICM \_ 2-2**</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="b0287-120">層級2。</span><span class="sxs-lookup"><span data-stu-id="b0287-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="b0287-121"><dt>**ICM \_ 2- \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="b0287-122">層級2。5</span><span class="sxs-lookup"><span data-stu-id="b0287-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="b0287-123"><dt>**ICM \_ 級別 2 \_ SUI**</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="b0287-124">特殊的 UI。</span><span class="sxs-lookup"><span data-stu-id="b0287-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="b0287-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0287-125">Requirements</span></span>



| <span data-ttu-id="b0287-126">需求</span><span class="sxs-lookup"><span data-stu-id="b0287-126">Requirement</span></span> | <span data-ttu-id="b0287-127">值</span><span class="sxs-lookup"><span data-stu-id="b0287-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0287-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0287-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b0287-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0287-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0287-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0287-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b0287-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0287-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0287-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b0287-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0287-133"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0287-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





