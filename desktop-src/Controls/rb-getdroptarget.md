---
title: 'RB_GETDROPTARGET 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項的 IDropTarget 介面指標。
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466077"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="c91de-104">RB \_ GETDROPTARGET 訊息</span><span class="sxs-lookup"><span data-stu-id="c91de-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="c91de-105">抓取 Rebar 控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c91de-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="c91de-106">參數</span><span class="sxs-lookup"><span data-stu-id="c91de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c91de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c91de-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c91de-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c91de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c91de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c91de-110">[**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget)指標的指標，該指標會接收介面指標。</span><span class="sxs-lookup"><span data-stu-id="c91de-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="c91de-111">當不再需要時，呼叫端會負責呼叫這個指標的 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="c91de-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91de-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c91de-112">Return value</span></span>

<span data-ttu-id="c91de-113">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c91de-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91de-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c91de-114">Requirements</span></span>



| <span data-ttu-id="c91de-115">需求</span><span class="sxs-lookup"><span data-stu-id="c91de-115">Requirement</span></span> | <span data-ttu-id="c91de-116">值</span><span class="sxs-lookup"><span data-stu-id="c91de-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c91de-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c91de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c91de-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c91de-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c91de-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c91de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c91de-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c91de-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c91de-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c91de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c91de-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c91de-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

