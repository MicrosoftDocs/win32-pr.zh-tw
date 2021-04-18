---
title: 'CBEM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 取得指派給 ComboBoxEx 控制項之影像清單的控制碼。
ms.assetid: d577f920-b8f7-4d51-9507-765b7f925408
keywords:
- CBEM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d143b8483fb5fb97ebd65fa2a98640089f6d548
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965108"
---
# <a name="cbem_getimagelist-message"></a><span data-ttu-id="18109-104">CBEM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="18109-104">CBEM\_GETIMAGELIST message</span></span>

<span data-ttu-id="18109-105">取得指派給 ComboBoxEx 控制項之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18109-105">Gets the handle to an image list assigned to a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="18109-106">參數</span><span class="sxs-lookup"><span data-stu-id="18109-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18109-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18109-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="18109-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18109-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="18109-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18109-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="18109-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18109-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18109-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="18109-111">Return value</span></span>

<span data-ttu-id="18109-112">如果成功，則傳回指派給控制項之影像清單的控制碼; 否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="18109-112">Returns the handle to the image list assigned to the control if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="18109-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="18109-113">Requirements</span></span>



| <span data-ttu-id="18109-114">需求</span><span class="sxs-lookup"><span data-stu-id="18109-114">Requirement</span></span> | <span data-ttu-id="18109-115">值</span><span class="sxs-lookup"><span data-stu-id="18109-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18109-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18109-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18109-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18109-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18109-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18109-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18109-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18109-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18109-120">標頭</span><span class="sxs-lookup"><span data-stu-id="18109-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="18109-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="18109-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





