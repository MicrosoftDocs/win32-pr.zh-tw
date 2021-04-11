---
title: 'EM_GETOLEINTERFACE 訊息 (Richedit .h) '
description: 抓取 IRichEditOle 物件，此物件可讓用戶端用來存取 rich edit 控制項的元件物件模型， (COM) 功能。
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104819"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="b2e34-104">EM \_ GETOLEINTERFACE 訊息</span><span class="sxs-lookup"><span data-stu-id="b2e34-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="b2e34-105">抓取 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 物件，此物件可讓用戶端用來存取 rich edit 控制項的元件物件模型， (COM) 功能。</span><span class="sxs-lookup"><span data-stu-id="b2e34-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2e34-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2e34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e34-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="b2e34-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b2e34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2e34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e34-110">接收 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 物件之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="b2e34-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="b2e34-111">控制項會在傳回之前呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法，因此呼叫的應用程式必須在物件完成時呼叫 [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法。</span><span class="sxs-lookup"><span data-stu-id="b2e34-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e34-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2e34-112">Return value</span></span>

<span data-ttu-id="b2e34-113">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="b2e34-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b2e34-114">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b2e34-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e34-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2e34-115">Requirements</span></span>



| <span data-ttu-id="b2e34-116">需求</span><span class="sxs-lookup"><span data-stu-id="b2e34-116">Requirement</span></span> | <span data-ttu-id="b2e34-117">值</span><span class="sxs-lookup"><span data-stu-id="b2e34-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e34-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2e34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e34-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2e34-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2e34-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2e34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e34-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2e34-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2e34-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b2e34-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e34-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e34-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e34-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2e34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e34-125">**IRichEditOle**</span><span class="sxs-lookup"><span data-stu-id="b2e34-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

