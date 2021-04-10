---
title: 'TB_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與工具列相關聯之工具提示控制項（如果有的話）的控制碼。
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025178"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="4bf30-104">TB \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="4bf30-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="4bf30-105">抓取與工具列相關聯之工具提示控制項（如果有的話）的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4bf30-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bf30-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bf30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bf30-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4bf30-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4bf30-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4bf30-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bf30-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4bf30-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4bf30-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf30-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bf30-111">Return value</span></span>

<span data-ttu-id="4bf30-112">傳回工具提示控制項的控制碼; 如果工具列沒有相關聯的工具提示，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="4bf30-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf30-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bf30-113">Requirements</span></span>



| <span data-ttu-id="4bf30-114">需求</span><span class="sxs-lookup"><span data-stu-id="4bf30-114">Requirement</span></span> | <span data-ttu-id="4bf30-115">值</span><span class="sxs-lookup"><span data-stu-id="4bf30-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf30-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bf30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf30-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bf30-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bf30-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bf30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf30-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bf30-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bf30-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4bf30-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bf30-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf30-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





