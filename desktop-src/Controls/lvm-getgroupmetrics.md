---
title: 'LVM_GETGROUPMETRICS 訊息 (Commctrl .h) '
description: 取得群組顯示的相關資訊。
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934902"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="ae885-104">LVM \_ GETGROUPMETRICS 訊息</span><span class="sxs-lookup"><span data-stu-id="ae885-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="ae885-105">取得群組顯示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae885-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae885-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae885-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae885-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae885-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ae885-108">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ae885-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="ae885-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae885-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae885-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a>結構的指標，此結構會接收已抓取的度量。</span><span class="sxs-lookup"><span data-stu-id="ae885-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae885-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae885-111">Return value</span></span>

<span data-ttu-id="ae885-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="ae885-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae885-113">備註</span><span class="sxs-lookup"><span data-stu-id="ae885-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae885-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ae885-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ae885-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ae885-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae885-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae885-116">Requirements</span></span>



| <span data-ttu-id="ae885-117">需求</span><span class="sxs-lookup"><span data-stu-id="ae885-117">Requirement</span></span> | <span data-ttu-id="ae885-118">值</span><span class="sxs-lookup"><span data-stu-id="ae885-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae885-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae885-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae885-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae885-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae885-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae885-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae885-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae885-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae885-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ae885-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae885-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae885-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





