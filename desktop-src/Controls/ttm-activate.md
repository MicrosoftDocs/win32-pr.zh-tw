---
title: 'TTM_ACTI加值稅E 訊息 (Commctrl .h) '
description: 啟用或停用工具提示控制項。
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- TTM_ACTI加值稅E message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e200b769cd3d9e07cb63a5a540960bcc707f862d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025116"
---
# <a name="ttm_activate-message"></a><span data-ttu-id="8e790-104">TTM \_ 啟動訊息</span><span class="sxs-lookup"><span data-stu-id="8e790-104">TTM\_ACTIVATE message</span></span>

<span data-ttu-id="8e790-105">啟用或停用工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="8e790-105">Activates or deactivates a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e790-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e790-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e790-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e790-108">啟用旗標。</span><span class="sxs-lookup"><span data-stu-id="8e790-108">Activation flag.</span></span> <span data-ttu-id="8e790-109">如果此參數為 **TRUE**，則會啟用工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="8e790-109">If this parameter is **TRUE**, the tooltip control is activated.</span></span> <span data-ttu-id="8e790-110">如果為 **FALSE**，則會停用工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="8e790-110">If it is **FALSE**, the tooltip control is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="8e790-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e790-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8e790-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8e790-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e790-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e790-113">Return value</span></span>

<span data-ttu-id="8e790-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="8e790-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e790-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e790-115">Requirements</span></span>



| <span data-ttu-id="8e790-116">需求</span><span class="sxs-lookup"><span data-stu-id="8e790-116">Requirement</span></span> | <span data-ttu-id="8e790-117">值</span><span class="sxs-lookup"><span data-stu-id="8e790-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e790-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e790-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e790-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e790-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e790-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e790-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e790-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e790-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e790-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8e790-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e790-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





