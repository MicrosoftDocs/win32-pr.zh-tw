---
title: 'EM_GETTOUCHOPTIONS 訊息 (Richedit .h) '
description: 抓取與 rich edit 控制項相關聯的觸控選項。
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025335"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="612ab-104">EM \_ GETTOUCHOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="612ab-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="612ab-105">抓取與 rich edit 控制項相關聯的觸控選項。</span><span class="sxs-lookup"><span data-stu-id="612ab-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="612ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="612ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="612ab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="612ab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="612ab-108">要取出的觸控選項。</span><span class="sxs-lookup"><span data-stu-id="612ab-108">The touch options to retrieve.</span></span> <span data-ttu-id="612ab-109">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="612ab-109">It can be one of the following values.</span></span>



| <span data-ttu-id="612ab-110">值</span><span class="sxs-lookup"><span data-stu-id="612ab-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="612ab-111">意義</span><span class="sxs-lookup"><span data-stu-id="612ab-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="612ab-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="612ab-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="612ab-113">抓取觸控 grippers 是否可見。</span><span class="sxs-lookup"><span data-stu-id="612ab-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="612ab-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="612ab-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="612ab-115">未執行此旗標的抓取。</span><span class="sxs-lookup"><span data-stu-id="612ab-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="612ab-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="612ab-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="612ab-117">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="612ab-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="612ab-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="612ab-118">Return value</span></span>

<span data-ttu-id="612ab-119">傳回 *wParam* 參數所指定之選項的值。</span><span class="sxs-lookup"><span data-stu-id="612ab-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="612ab-120">如果 *wParam* 是 **RTO \_ SHOWHANDLES** 且觸控 grippers 可見則為非零，否則為零。</span><span class="sxs-lookup"><span data-stu-id="612ab-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="612ab-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="612ab-121">Requirements</span></span>



| <span data-ttu-id="612ab-122">需求</span><span class="sxs-lookup"><span data-stu-id="612ab-122">Requirement</span></span> | <span data-ttu-id="612ab-123">值</span><span class="sxs-lookup"><span data-stu-id="612ab-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="612ab-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="612ab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="612ab-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="612ab-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="612ab-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="612ab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="612ab-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="612ab-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="612ab-128">標頭</span><span class="sxs-lookup"><span data-stu-id="612ab-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="612ab-129"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="612ab-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="612ab-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="612ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612ab-131">**EM \_ SETTOUCHOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="612ab-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





