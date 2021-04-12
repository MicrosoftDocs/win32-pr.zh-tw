---
title: 'LVM_GETHEADER 訊息 (Commctrl .h) '
description: 取得清單視圖控制項所使用之標題控制項的控制碼。 您可以明確地傳送此訊息，或使用 ListView \_ messageheaders 宏。
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024664"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="0c8b2-105">LVM \_ messageheaders 訊息</span><span class="sxs-lookup"><span data-stu-id="0c8b2-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="0c8b2-106">取得清單視圖控制項所使用之標題控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c8b2-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="0c8b2-107">您可以明確地傳送此訊息，或使用 [**ListView \_ messageheaders**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) 宏。</span><span class="sxs-lookup"><span data-stu-id="0c8b2-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c8b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="0c8b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c8b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c8b2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0c8b2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0c8b2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0c8b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c8b2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c8b2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0c8b2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c8b2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c8b2-113">Return value</span></span>

<span data-ttu-id="0c8b2-114">將控制碼傳回至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="0c8b2-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8b2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c8b2-115">Requirements</span></span>



| <span data-ttu-id="0c8b2-116">需求</span><span class="sxs-lookup"><span data-stu-id="0c8b2-116">Requirement</span></span> | <span data-ttu-id="0c8b2-117">值</span><span class="sxs-lookup"><span data-stu-id="0c8b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8b2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c8b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c8b2-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c8b2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c8b2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c8b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c8b2-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c8b2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c8b2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0c8b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c8b2-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8b2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





