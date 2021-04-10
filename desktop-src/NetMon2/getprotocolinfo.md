---
description: GetProtocolInfo 函式會傳回通訊協定資訊值的指標。
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: 'GetProtocolInfo 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936616"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="8d373-103">GetProtocolInfo 函式</span><span class="sxs-lookup"><span data-stu-id="8d373-103">GetProtocolInfo function</span></span>

<span data-ttu-id="8d373-104">**GetProtocolInfo** 函式會傳回通訊協定資訊值的指標。</span><span class="sxs-lookup"><span data-stu-id="8d373-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d373-105">語法</span><span class="sxs-lookup"><span data-stu-id="8d373-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="8d373-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d373-107">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d373-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d373-108">通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8d373-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d373-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d373-109">Return value</span></span>

<span data-ttu-id="8d373-110">如果函式成功，則傳回值為通訊協定資訊值的指標。</span><span class="sxs-lookup"><span data-stu-id="8d373-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="8d373-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d373-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d373-112">備註</span><span class="sxs-lookup"><span data-stu-id="8d373-112">Remarks</span></span>

<span data-ttu-id="8d373-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProtocolInfo** 函數。</span><span class="sxs-lookup"><span data-stu-id="8d373-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d373-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d373-114">Requirements</span></span>



| <span data-ttu-id="8d373-115">需求</span><span class="sxs-lookup"><span data-stu-id="8d373-115">Requirement</span></span> | <span data-ttu-id="8d373-116">值</span><span class="sxs-lookup"><span data-stu-id="8d373-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d373-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d373-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d373-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d373-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8d373-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d373-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d373-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d373-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d373-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8d373-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d373-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8d373-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d373-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d373-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d373-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d373-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d373-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d373-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d373-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d373-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




