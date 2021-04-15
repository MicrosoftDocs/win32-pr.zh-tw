---
description: GetCaptureTimeStamp 函式會傳回 capture 開始錄製畫面格的時間和日期。
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: 'GetCaptureTimeStamp 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510975"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="23b0b-103">GetCaptureTimeStamp 函式</span><span class="sxs-lookup"><span data-stu-id="23b0b-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="23b0b-104">**GetCaptureTimeStamp** 函式會傳回 capture 開始錄製畫面格的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="23b0b-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="23b0b-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="23b0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="23b0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b0b-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23b0b-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b0b-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="23b0b-108">Handle to the capture.</span></span> <span data-ttu-id="23b0b-109">如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureTimeStamp** 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="23b0b-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b0b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="23b0b-110">Return value</span></span>

<span data-ttu-id="23b0b-111">如果函式成功，則傳回值是 [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="23b0b-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="23b0b-112">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="23b0b-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b0b-113">備註</span><span class="sxs-lookup"><span data-stu-id="23b0b-113">Remarks</span></span>

<span data-ttu-id="23b0b-114">**GetCaptureTimeStamp** 函式會傳回網路封包提供者 (NPP) 開始收集資料的時間，而不是當專家載入要分析的捕獲時。</span><span class="sxs-lookup"><span data-stu-id="23b0b-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="23b0b-115">請勿覆寫 **SYSTEMTIME** 結構中的資料。</span><span class="sxs-lookup"><span data-stu-id="23b0b-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="23b0b-116">資料是捕捉的一部分。</span><span class="sxs-lookup"><span data-stu-id="23b0b-116">The data is part of the capture.</span></span> <span data-ttu-id="23b0b-117">嘗試修改資料會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="23b0b-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="23b0b-118">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureTimeStamp** 函數。</span><span class="sxs-lookup"><span data-stu-id="23b0b-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b0b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="23b0b-119">Requirements</span></span>



| <span data-ttu-id="23b0b-120">需求</span><span class="sxs-lookup"><span data-stu-id="23b0b-120">Requirement</span></span> | <span data-ttu-id="23b0b-121">值</span><span class="sxs-lookup"><span data-stu-id="23b0b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23b0b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23b0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23b0b-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23b0b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="23b0b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23b0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23b0b-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23b0b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23b0b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23b0b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b0b-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="23b0b-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="23b0b-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="23b0b-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="23b0b-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b0b-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="23b0b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="23b0b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b0b-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b0b-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b0b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23b0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b0b-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="23b0b-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

