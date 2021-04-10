---
title: 'RB_GETBARINFO 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項及其所使用影像清單的相關資訊。
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- RB_GETBARINFO message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025281"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="ecc18-104">RB \_ GETBARINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="ecc18-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="ecc18-105">抓取 Rebar 控制項及其所使用影像清單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ecc18-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecc18-106">參數</span><span class="sxs-lookup"><span data-stu-id="ecc18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc18-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecc18-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ecc18-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ecc18-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ecc18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecc18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecc18-110">[**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)結構的指標，此結構會接收 Rebar 控制項資訊。</span><span class="sxs-lookup"><span data-stu-id="ecc18-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="ecc18-111">在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARINFO) 。</span><span class="sxs-lookup"><span data-stu-id="ecc18-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc18-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecc18-112">Return value</span></span>

<span data-ttu-id="ecc18-113">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="ecc18-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc18-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecc18-114">Requirements</span></span>



| <span data-ttu-id="ecc18-115">需求</span><span class="sxs-lookup"><span data-stu-id="ecc18-115">Requirement</span></span> | <span data-ttu-id="ecc18-116">值</span><span class="sxs-lookup"><span data-stu-id="ecc18-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc18-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecc18-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc18-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecc18-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecc18-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecc18-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc18-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecc18-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecc18-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ecc18-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc18-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc18-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





