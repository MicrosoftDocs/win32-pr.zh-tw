---
title: 'LVM_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定插入點的色彩。
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- LVM_SETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933917"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="e11af-104">LVM \_ SETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="e11af-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="e11af-105">設定插入點的色彩。</span><span class="sxs-lookup"><span data-stu-id="e11af-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="e11af-106">參數</span><span class="sxs-lookup"><span data-stu-id="e11af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e11af-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e11af-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e11af-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e11af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e11af-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e11af-110">**COLORREF** 結構，指定要設定插入點的色彩。</span><span class="sxs-lookup"><span data-stu-id="e11af-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11af-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e11af-111">Return value</span></span>

<span data-ttu-id="e11af-112">傳回設定為上一個色彩的 **COLORREF** 結構。</span><span class="sxs-lookup"><span data-stu-id="e11af-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11af-113">備註</span><span class="sxs-lookup"><span data-stu-id="e11af-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e11af-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e11af-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e11af-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e11af-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e11af-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e11af-116">Requirements</span></span>



| <span data-ttu-id="e11af-117">需求</span><span class="sxs-lookup"><span data-stu-id="e11af-117">Requirement</span></span> | <span data-ttu-id="e11af-118">值</span><span class="sxs-lookup"><span data-stu-id="e11af-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e11af-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e11af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e11af-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e11af-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e11af-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e11af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e11af-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e11af-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e11af-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e11af-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e11af-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e11af-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





