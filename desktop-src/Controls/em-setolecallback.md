---
title: 'EM_SETOLECALLBACK 訊息 (Richedit .h) '
description: 提供 rich edit 控制項的 IRichEditOleCallback 物件，讓控制項用來從用戶端取得 OLE 相關的資源和資訊。
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934545"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="bdb17-104">EM \_ SETOLECALLBACK 訊息</span><span class="sxs-lookup"><span data-stu-id="bdb17-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="bdb17-105">提供 rich edit 控制項的 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 物件，讓控制項用來從用戶端取得 OLE 相關的資源和資訊。</span><span class="sxs-lookup"><span data-stu-id="bdb17-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdb17-106">參數</span><span class="sxs-lookup"><span data-stu-id="bdb17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdb17-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb17-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="bdb17-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bdb17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdb17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb17-110">[**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="bdb17-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="bdb17-111">控制項會在傳回之前呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法。</span><span class="sxs-lookup"><span data-stu-id="bdb17-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb17-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdb17-112">Return value</span></span>

<span data-ttu-id="bdb17-113">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="bdb17-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bdb17-114">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="bdb17-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb17-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdb17-115">Requirements</span></span>



| <span data-ttu-id="bdb17-116">需求</span><span class="sxs-lookup"><span data-stu-id="bdb17-116">Requirement</span></span> | <span data-ttu-id="bdb17-117">值</span><span class="sxs-lookup"><span data-stu-id="bdb17-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb17-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdb17-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb17-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdb17-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdb17-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdb17-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb17-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdb17-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdb17-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bdb17-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb17-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb17-123"><dt>Richedit.h</dt></span></span> </dl> |



 

