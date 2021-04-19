---
description: GetProtocolStartOffsetHandle 函式會傳回指定通訊協定的框架位移。
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: 'GetProtocolStartOffsetHandle 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992399"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="d8cd7-103">GetProtocolStartOffsetHandle 函式</span><span class="sxs-lookup"><span data-stu-id="d8cd7-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="d8cd7-104">**GetProtocolStartOffsetHandle** 函式會傳回指定通訊協定的框架位移。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8cd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8cd7-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d8cd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8cd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8cd7-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8cd7-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cd7-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d8cd7-109">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8cd7-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cd7-110">通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8cd7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8cd7-111">Return value</span></span>

<span data-ttu-id="d8cd7-112">如果函式成功，則傳回值是以位元組為單位的框架位移。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="d8cd7-113">如果函式不成功，則傳回值為一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8cd7-114">備註</span><span class="sxs-lookup"><span data-stu-id="d8cd7-114">Remarks</span></span>

<span data-ttu-id="d8cd7-115">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProtocolStartOffsetHandle** 函數。</span><span class="sxs-lookup"><span data-stu-id="d8cd7-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8cd7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8cd7-116">Requirements</span></span>



| <span data-ttu-id="d8cd7-117">需求</span><span class="sxs-lookup"><span data-stu-id="d8cd7-117">Requirement</span></span> | <span data-ttu-id="d8cd7-118">值</span><span class="sxs-lookup"><span data-stu-id="d8cd7-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d8cd7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8cd7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8cd7-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8cd7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d8cd7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8cd7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8cd7-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8cd7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d8cd7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d8cd7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8cd7-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d8cd7-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d8cd7-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8cd7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8cd7-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8cd7-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8cd7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d8cd7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8cd7-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8cd7-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




