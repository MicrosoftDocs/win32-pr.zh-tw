---
title: 'IPM_ISBLANK 訊息 (Commctrl .h) '
description: 判斷 IP 位址控制項中的所有欄位是否為空白。
ms.assetid: 6e35b848-943a-4475-890a-01fc3d8ed97d
keywords:
- IPM_ISBLANK message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_ISBLANK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f5a33ee3c35779a02cdfcb0fcb7066098f3160
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843888"
---
# <a name="ipm_isblank-message"></a><span data-ttu-id="4f4eb-104">IPM \_ ISBLANK 訊息</span><span class="sxs-lookup"><span data-stu-id="4f4eb-104">IPM\_ISBLANK message</span></span>

<span data-ttu-id="4f4eb-105">判斷 IP 位址控制項中的所有欄位是否為空白。</span><span class="sxs-lookup"><span data-stu-id="4f4eb-105">Determines if all fields in the IP address control are blank.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f4eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f4eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f4eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f4eb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4f4eb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4f4eb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4f4eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f4eb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4f4eb-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4f4eb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f4eb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f4eb-111">Return value</span></span>

<span data-ttu-id="4f4eb-112">如果所有欄位都是空白，則會傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4f4eb-112">Returns nonzero if all fields are blank, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4eb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f4eb-113">Requirements</span></span>



| <span data-ttu-id="4f4eb-114">需求</span><span class="sxs-lookup"><span data-stu-id="4f4eb-114">Requirement</span></span> | <span data-ttu-id="4f4eb-115">值</span><span class="sxs-lookup"><span data-stu-id="4f4eb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4eb-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f4eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4eb-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f4eb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f4eb-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f4eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4eb-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f4eb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f4eb-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4f4eb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f4eb-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4eb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





