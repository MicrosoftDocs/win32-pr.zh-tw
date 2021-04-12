---
title: 'TB_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項與工具列產生關聯。
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024850"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="f1aec-104">TB \_ SETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="f1aec-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="f1aec-105">將工具提示控制項與工具列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f1aec-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1aec-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1aec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1aec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1aec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1aec-108">工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f1aec-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="f1aec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1aec-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f1aec-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f1aec-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1aec-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1aec-111">Return value</span></span>

<span data-ttu-id="f1aec-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f1aec-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1aec-113">備註</span><span class="sxs-lookup"><span data-stu-id="f1aec-113">Remarks</span></span>

<span data-ttu-id="f1aec-114">在傳送 **TB \_ SETTOOLTIPS** 訊息之前新增至工具列的任何按鈕，都不會向工具提示控制項註冊。</span><span class="sxs-lookup"><span data-stu-id="f1aec-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1aec-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1aec-115">Requirements</span></span>



| <span data-ttu-id="f1aec-116">需求</span><span class="sxs-lookup"><span data-stu-id="f1aec-116">Requirement</span></span> | <span data-ttu-id="f1aec-117">值</span><span class="sxs-lookup"><span data-stu-id="f1aec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1aec-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1aec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f1aec-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1aec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1aec-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1aec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f1aec-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1aec-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1aec-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f1aec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1aec-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1aec-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





