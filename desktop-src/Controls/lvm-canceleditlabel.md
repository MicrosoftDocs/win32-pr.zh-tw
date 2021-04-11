---
title: 'LVM_CANCELEDITLABEL 訊息 (Commctrl .h) '
description: 取消專案文字編輯作業。
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- LVM_CANCELEDITLABEL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093856"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="f68f9-104">LVM \_ CANCELEDITLABEL 訊息</span><span class="sxs-lookup"><span data-stu-id="f68f9-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="f68f9-105">取消專案文字編輯作業。</span><span class="sxs-lookup"><span data-stu-id="f68f9-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="f68f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="f68f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f68f9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f68f9-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f68f9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f68f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f68f9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f68f9-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f68f9-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f68f9-111">備註</span><span class="sxs-lookup"><span data-stu-id="f68f9-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f68f9-112">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="f68f9-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f68f9-113">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f68f9-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="f68f9-114">這則訊息會導致傳送 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="f68f9-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f68f9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f68f9-115">Requirements</span></span>



| <span data-ttu-id="f68f9-116">需求</span><span class="sxs-lookup"><span data-stu-id="f68f9-116">Requirement</span></span> | <span data-ttu-id="f68f9-117">值</span><span class="sxs-lookup"><span data-stu-id="f68f9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f68f9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f68f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f68f9-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f68f9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f68f9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f68f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f68f9-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f68f9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f68f9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f68f9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f68f9-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f68f9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





