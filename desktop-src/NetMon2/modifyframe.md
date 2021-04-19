---
description: ModifyFrame 函式會使用新的資料來改變現有的框架。
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: 'ModifyFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970200"
---
# <a name="modifyframe-function"></a><span data-ttu-id="9aac4-103">ModifyFrame 函式</span><span class="sxs-lookup"><span data-stu-id="9aac4-103">ModifyFrame function</span></span>

<span data-ttu-id="9aac4-104">**ModifyFrame** 函式會使用新的資料來改變現有的框架。</span><span class="sxs-lookup"><span data-stu-id="9aac4-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aac4-105">語法</span><span class="sxs-lookup"><span data-stu-id="9aac4-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="9aac4-106">參數</span><span class="sxs-lookup"><span data-stu-id="9aac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aac4-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac4-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aac4-108">Handle to the capture.</span></span> <span data-ttu-id="9aac4-109">如需取得 capture 控制碼的詳細資訊，請參閱本 **ModifyFrame** 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="9aac4-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="9aac4-110">*FrameNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac4-111">框架索引編號。</span><span class="sxs-lookup"><span data-stu-id="9aac4-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="9aac4-112">*FrameData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac4-113">位元組陣列的指標，其中包含新的框架資料。</span><span class="sxs-lookup"><span data-stu-id="9aac4-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="9aac4-114">*FrameLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac4-115">新資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9aac4-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9aac4-116">*時間戳記* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac4-117">指出框架何時修改的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="9aac4-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aac4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9aac4-118">Return value</span></span>

<span data-ttu-id="9aac4-119">如果函式成功，則傳回值是新框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9aac4-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="9aac4-120">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9aac4-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aac4-121">備註</span><span class="sxs-lookup"><span data-stu-id="9aac4-121">Remarks</span></span>

<span data-ttu-id="9aac4-122">如果呼叫成功， **ModifyFrame** 函式會終結原始框架。</span><span class="sxs-lookup"><span data-stu-id="9aac4-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="9aac4-123">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **ModifyFrame** 函數。</span><span class="sxs-lookup"><span data-stu-id="9aac4-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aac4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aac4-124">Requirements</span></span>



| <span data-ttu-id="9aac4-125">需求</span><span class="sxs-lookup"><span data-stu-id="9aac4-125">Requirement</span></span> | <span data-ttu-id="9aac4-126">值</span><span class="sxs-lookup"><span data-stu-id="9aac4-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9aac4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aac4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9aac4-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9aac4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aac4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9aac4-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aac4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9aac4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9aac4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aac4-132"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9aac4-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9aac4-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9aac4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9aac4-134"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aac4-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9aac4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9aac4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aac4-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aac4-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




