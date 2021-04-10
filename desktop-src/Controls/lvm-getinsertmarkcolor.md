---
title: 'LVM_GETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 抓取插入點的色彩。
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- LVM_GETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106679"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="eeaef-104">LVM \_ GETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="eeaef-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="eeaef-105">抓取插入點的色彩。</span><span class="sxs-lookup"><span data-stu-id="eeaef-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="eeaef-106">參數</span><span class="sxs-lookup"><span data-stu-id="eeaef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeaef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeaef-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eeaef-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eeaef-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eeaef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeaef-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eeaef-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eeaef-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeaef-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeaef-111">Return value</span></span>

<span data-ttu-id="eeaef-112">傳回 **COLORREF** 結構，其中包含插入點的色彩。</span><span class="sxs-lookup"><span data-stu-id="eeaef-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeaef-113">備註</span><span class="sxs-lookup"><span data-stu-id="eeaef-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eeaef-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eeaef-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="eeaef-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="eeaef-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eeaef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeaef-116">Requirements</span></span>



| <span data-ttu-id="eeaef-117">需求</span><span class="sxs-lookup"><span data-stu-id="eeaef-117">Requirement</span></span> | <span data-ttu-id="eeaef-118">值</span><span class="sxs-lookup"><span data-stu-id="eeaef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeaef-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeaef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eeaef-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeaef-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeaef-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeaef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eeaef-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeaef-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eeaef-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eeaef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeaef-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeaef-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





