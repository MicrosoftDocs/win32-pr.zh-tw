---
title: 'TB_GETBUTTON 訊息 (Commctrl .h) '
description: 抓取工具列中指定之按鈕的相關資訊。
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686659"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="5b3d2-104">TB \_ GETBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="5b3d2-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="5b3d2-105">抓取工具列中指定之按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b3d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b3d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b3d2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b3d2-108">以零為基底的按鈕索引，用來取得資訊。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b3d2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b3d2-110">接收按鈕資訊之 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3d2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b3d2-111">Return value</span></span>

<span data-ttu-id="5b3d2-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3d2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b3d2-113">Requirements</span></span>



| <span data-ttu-id="5b3d2-114">需求</span><span class="sxs-lookup"><span data-stu-id="5b3d2-114">Requirement</span></span> | <span data-ttu-id="5b3d2-115">值</span><span class="sxs-lookup"><span data-stu-id="5b3d2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b3d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3d2-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3d2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b3d2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b3d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3d2-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3d2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b3d2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5b3d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b3d2-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





