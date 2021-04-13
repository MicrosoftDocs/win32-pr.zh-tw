---
title: 'WsSetAutoFail 函式 (WebServicesDebug) '
description: 設定下一個插入失敗的點。 這是僅限 DEBUG 函數。
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- 適用于 Windows 的 WsSetAutoFail 函式 Web 服務
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509083"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="217d2-105">WsSetAutoFail 函式</span><span class="sxs-lookup"><span data-stu-id="217d2-105">WsSetAutoFail function</span></span>

<span data-ttu-id="217d2-106">設定下一個插入失敗的點。</span><span class="sxs-lookup"><span data-stu-id="217d2-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="217d2-107">這是僅限 DEBUG 函數。</span><span class="sxs-lookup"><span data-stu-id="217d2-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="217d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="217d2-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="217d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="217d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217d2-110">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="217d2-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217d2-111">指定失敗前的作業開始發生的次數。</span><span class="sxs-lookup"><span data-stu-id="217d2-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="217d2-112">*錯誤* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="217d2-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="217d2-113">[WS \_ ERROR](ws-error.md)物件的指標，如果函式失敗，則應儲存錯誤的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="217d2-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217d2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="217d2-114">Return value</span></span>

<span data-ttu-id="217d2-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="217d2-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="217d2-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="217d2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="217d2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="217d2-117">Requirements</span></span>



| <span data-ttu-id="217d2-118">需求</span><span class="sxs-lookup"><span data-stu-id="217d2-118">Requirement</span></span> | <span data-ttu-id="217d2-119">值</span><span class="sxs-lookup"><span data-stu-id="217d2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="217d2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="217d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="217d2-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="217d2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="217d2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="217d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="217d2-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="217d2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="217d2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="217d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="217d2-125"><dt>WebServicesDebug。h</dt></span><span class="sxs-lookup"><span data-stu-id="217d2-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





