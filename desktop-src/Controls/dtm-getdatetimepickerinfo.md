---
title: 'DTM_GETDATETIMEPICKERINFO 訊息 (Commctrl .h) '
description: 取得 (DTP) 控制項之日期和時間選擇器的資訊。
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464433"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="b7922-104">DTM \_ GETDATETIMEPICKERINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="b7922-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="b7922-105">取得 (DTP) 控制項之日期和時間選擇器的資訊。</span><span class="sxs-lookup"><span data-stu-id="b7922-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7922-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7922-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7922-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7922-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b7922-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b7922-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7922-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="b7922-110">要接收資訊的 <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> 指標。</span><span class="sxs-lookup"><span data-stu-id="b7922-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="b7922-111">呼叫端負責配置此結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b7922-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="b7922-112">將結構的 **cbSize** 成員設定為 SIZEOF (DATETIMEPICKERINFO) ，然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b7922-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7922-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7922-113">Return value</span></span>

<span data-ttu-id="b7922-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b7922-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7922-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7922-115">Requirements</span></span>



| <span data-ttu-id="b7922-116">需求</span><span class="sxs-lookup"><span data-stu-id="b7922-116">Requirement</span></span> | <span data-ttu-id="b7922-117">值</span><span class="sxs-lookup"><span data-stu-id="b7922-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7922-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7922-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7922-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7922-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7922-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7922-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7922-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7922-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7922-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b7922-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7922-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7922-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





