---
title: 'TB_REPLACEBITMAP 訊息 (Commctrl .h) '
description: 以新的點陣圖取代現有的點陣圖。
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843983"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="82b9a-104">TB \_ REPLACEBITMAP 訊息</span><span class="sxs-lookup"><span data-stu-id="82b9a-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="82b9a-105">以新的點陣圖取代現有的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="82b9a-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="82b9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="82b9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82b9a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="82b9a-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="82b9a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="82b9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82b9a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82b9a-110">[**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap)結構的指標，其中包含要取代的點陣圖資訊和新的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="82b9a-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b9a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82b9a-111">Return value</span></span>

<span data-ttu-id="82b9a-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="82b9a-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b9a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b9a-113">Requirements</span></span>



| <span data-ttu-id="82b9a-114">需求</span><span class="sxs-lookup"><span data-stu-id="82b9a-114">Requirement</span></span> | <span data-ttu-id="82b9a-115">值</span><span class="sxs-lookup"><span data-stu-id="82b9a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82b9a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82b9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82b9a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b9a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82b9a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82b9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82b9a-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b9a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82b9a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="82b9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b9a-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="82b9a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





