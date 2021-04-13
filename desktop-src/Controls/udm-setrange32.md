---
title: 'UDM_SETRANGE32 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的32位範圍。
ms.assetid: 6167db8f-a823-44d3-a515-888b6d1a39c2
keywords:
- UDM_SETRANGE32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80de7c9583a10abe7c62ec5a074dcfa91a59cc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508899"
---
# <a name="udm_setrange32-message"></a><span data-ttu-id="ff027-104">UDM \_ SETRANGE32 訊息</span><span class="sxs-lookup"><span data-stu-id="ff027-104">UDM\_SETRANGE32 message</span></span>

<span data-ttu-id="ff027-105">設定上下按鈕控制項的32位範圍。</span><span class="sxs-lookup"><span data-stu-id="ff027-105">Sets the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff027-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff027-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff027-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff027-108">帶正負號的整數值，表示上下按鈕控制項範圍的新下限。</span><span class="sxs-lookup"><span data-stu-id="ff027-108">Signed integer value that represents the new lower limit of the up-down control range.</span></span>

</dd> <dt>

<span data-ttu-id="ff027-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff027-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff027-110">帶正負號的整數值，表示上下按鈕控制項範圍的新上限。</span><span class="sxs-lookup"><span data-stu-id="ff027-110">Signed integer value that represents the new upper limit of the up-down control range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff027-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff027-111">Return value</span></span>

<span data-ttu-id="ff027-112">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="ff027-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff027-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff027-113">Requirements</span></span>



| <span data-ttu-id="ff027-114">需求</span><span class="sxs-lookup"><span data-stu-id="ff027-114">Requirement</span></span> | <span data-ttu-id="ff027-115">值</span><span class="sxs-lookup"><span data-stu-id="ff027-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff027-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff027-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff027-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff027-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff027-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff027-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff027-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff027-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff027-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ff027-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff027-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff027-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





