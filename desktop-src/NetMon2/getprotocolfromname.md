---
description: GetProtocolFromName 函式會將控制碼傳回給指定名稱的通訊協定。
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: 'GetProtocolFromName 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689715"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="27511-103">GetProtocolFromName 函式</span><span class="sxs-lookup"><span data-stu-id="27511-103">GetProtocolFromName function</span></span>

<span data-ttu-id="27511-104">**GetProtocolFromName** 函式會將控制碼傳回給指定名稱的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="27511-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="27511-105">語法</span><span class="sxs-lookup"><span data-stu-id="27511-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="27511-106">參數</span><span class="sxs-lookup"><span data-stu-id="27511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27511-107">*ProtocolName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27511-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27511-108">通訊協定名稱 (例如 IP) 。</span><span class="sxs-lookup"><span data-stu-id="27511-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27511-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="27511-109">Return value</span></span>

<span data-ttu-id="27511-110">如果函式成功，則傳回值為通訊協定控制碼。</span><span class="sxs-lookup"><span data-stu-id="27511-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="27511-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27511-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27511-112">備註</span><span class="sxs-lookup"><span data-stu-id="27511-112">Remarks</span></span>

<span data-ttu-id="27511-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProtocolFromName** 函數。</span><span class="sxs-lookup"><span data-stu-id="27511-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="27511-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="27511-114">Requirements</span></span>



| <span data-ttu-id="27511-115">需求</span><span class="sxs-lookup"><span data-stu-id="27511-115">Requirement</span></span> | <span data-ttu-id="27511-116">值</span><span class="sxs-lookup"><span data-stu-id="27511-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27511-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27511-117">Minimum supported client</span></span><br/> | <span data-ttu-id="27511-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27511-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="27511-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27511-119">Minimum supported server</span></span><br/> | <span data-ttu-id="27511-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27511-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="27511-121">標頭</span><span class="sxs-lookup"><span data-stu-id="27511-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="27511-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="27511-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="27511-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="27511-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="27511-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="27511-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="27511-125">DLL</span><span class="sxs-lookup"><span data-stu-id="27511-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27511-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27511-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




