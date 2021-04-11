---
description: AddressToString 函式會將位址轉換成字串。
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: 'AddressToString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115880"
---
# <a name="addresstostring-function"></a><span data-ttu-id="fe2a0-103">AddressToString 函式</span><span class="sxs-lookup"><span data-stu-id="fe2a0-103">AddressToString function</span></span>

<span data-ttu-id="fe2a0-104">**AddressToString** 函式會將位址轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="fe2a0-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe2a0-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="fe2a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe2a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2a0-107">*字串* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe2a0-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a0-108">位址轉換成的字串。</span><span class="sxs-lookup"><span data-stu-id="fe2a0-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a0-109">*lpAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe2a0-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a0-110">列印的位址。</span><span class="sxs-lookup"><span data-stu-id="fe2a0-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2a0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe2a0-111">Return value</span></span>

<span data-ttu-id="fe2a0-112">傳回值是轉換後字串的指標。</span><span class="sxs-lookup"><span data-stu-id="fe2a0-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe2a0-113">Requirements</span></span>



| <span data-ttu-id="fe2a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="fe2a0-114">Requirement</span></span> | <span data-ttu-id="fe2a0-115">值</span><span class="sxs-lookup"><span data-stu-id="fe2a0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2a0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe2a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2a0-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe2a0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fe2a0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe2a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2a0-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe2a0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe2a0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fe2a0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe2a0-121"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a0-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe2a0-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe2a0-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe2a0-123"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a0-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe2a0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fe2a0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe2a0-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a0-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




