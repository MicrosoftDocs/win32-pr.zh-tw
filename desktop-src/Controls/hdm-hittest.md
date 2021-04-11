---
title: 'HDM_HITTEST 訊息 (Commctrl .h) '
description: 測試點以判斷哪個標頭專案（如果有的話）位於指定的點。
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104483"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="33ac4-104">HDM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="33ac4-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="33ac4-105">測試點以判斷哪個標頭專案（如果有的話）位於指定的點。</span><span class="sxs-lookup"><span data-stu-id="33ac4-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="33ac4-106">參數</span><span class="sxs-lookup"><span data-stu-id="33ac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ac4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33ac4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33ac4-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="33ac4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33ac4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33ac4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33ac4-110">[**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo)結構的指標，其中包含要測試的位置，以及接收測試結果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33ac4-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ac4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="33ac4-111">Return value</span></span>

<span data-ttu-id="33ac4-112">傳回位於指定位置之專案的索引（如果有的話），否則傳回1。</span><span class="sxs-lookup"><span data-stu-id="33ac4-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ac4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="33ac4-113">Requirements</span></span>



| <span data-ttu-id="33ac4-114">需求</span><span class="sxs-lookup"><span data-stu-id="33ac4-114">Requirement</span></span> | <span data-ttu-id="33ac4-115">值</span><span class="sxs-lookup"><span data-stu-id="33ac4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33ac4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33ac4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33ac4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33ac4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33ac4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33ac4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="33ac4-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33ac4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33ac4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="33ac4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="33ac4-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33ac4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





