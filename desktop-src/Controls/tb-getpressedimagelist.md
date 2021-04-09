---
title: 'TB_GETPRESSEDIMAGELIST 訊息 (Commctrl .h) '
description: 取得工具列控制項用來顯示處於已按下狀態之按鈕的影像清單。
ms.assetid: 116d4212-48ea-4b00-a752-21e5e1f10e36
keywords:
- TB_GETPRESSEDIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3028b119eb7f84a66caf0b6978382cee569b4a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106440"
---
# <a name="tb_getpressedimagelist-message"></a><span data-ttu-id="67bec-104">TB \_ GETPRESSEDIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="67bec-104">TB\_GETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="67bec-105">取得工具列控制項用來顯示處於已按下狀態之按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="67bec-105">Gets the image list that a toolbar control uses to display buttons in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="67bec-106">參數</span><span class="sxs-lookup"><span data-stu-id="67bec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67bec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67bec-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67bec-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67bec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67bec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67bec-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67bec-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bec-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="67bec-111">Return value</span></span>

<span data-ttu-id="67bec-112">傳回影像清單的控制碼，如果未設定影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="67bec-112">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="67bec-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="67bec-113">Requirements</span></span>



| <span data-ttu-id="67bec-114">需求</span><span class="sxs-lookup"><span data-stu-id="67bec-114">Requirement</span></span> | <span data-ttu-id="67bec-115">值</span><span class="sxs-lookup"><span data-stu-id="67bec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67bec-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67bec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67bec-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67bec-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67bec-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67bec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67bec-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67bec-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67bec-120">標頭</span><span class="sxs-lookup"><span data-stu-id="67bec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67bec-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="67bec-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





