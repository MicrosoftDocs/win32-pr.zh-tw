---
title: 'RB_SETBANDWIDTH 訊息 (Commctrl .h) '
description: 設定停駐區的寬度。
ms.assetid: dca9dfe9-3e5a-40bb-8de7-a296e6be7d06
keywords:
- RB_SETBANDWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBANDWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790f42ab977cfc0554c9a0eca737d541e001b6c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466072"
---
# <a name="rb_setbandwidth-message"></a><span data-ttu-id="51e63-104">RB \_ SETBANDWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="51e63-104">RB\_SETBANDWIDTH message</span></span>

<span data-ttu-id="51e63-105">設定停駐區的寬度。</span><span class="sxs-lookup"><span data-stu-id="51e63-105">Sets the width for a docked band.</span></span>

## <a name="parameters"></a><span data-ttu-id="51e63-106">參數</span><span class="sxs-lookup"><span data-stu-id="51e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e63-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51e63-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e63-108">寬線的索引。</span><span class="sxs-lookup"><span data-stu-id="51e63-108">Index of the band.</span></span>

</dd> <dt>

<span data-ttu-id="51e63-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51e63-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e63-110">新的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="51e63-110">New width in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e63-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51e63-111">Return value</span></span>

<span data-ttu-id="51e63-112">如果已設定值，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="51e63-112">Returns **TRUE** if the value was set and **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e63-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="51e63-113">Requirements</span></span>



| <span data-ttu-id="51e63-114">需求</span><span class="sxs-lookup"><span data-stu-id="51e63-114">Requirement</span></span> | <span data-ttu-id="51e63-115">值</span><span class="sxs-lookup"><span data-stu-id="51e63-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51e63-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51e63-116">Minimum supported client</span></span><br/> | <span data-ttu-id="51e63-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51e63-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51e63-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51e63-118">Minimum supported server</span></span><br/> | <span data-ttu-id="51e63-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51e63-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51e63-120">標頭</span><span class="sxs-lookup"><span data-stu-id="51e63-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e63-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="51e63-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





