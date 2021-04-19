---
description: StringToAddress 函式會將字串轉換成位址。
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: 'StringToAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986862"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="18213-103">StringToAddress 函式</span><span class="sxs-lookup"><span data-stu-id="18213-103">StringToAddress function</span></span>

<span data-ttu-id="18213-104">**StringToAddress** 函式會將字串轉換成位址。</span><span class="sxs-lookup"><span data-stu-id="18213-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="18213-105">語法</span><span class="sxs-lookup"><span data-stu-id="18213-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="18213-106">參數</span><span class="sxs-lookup"><span data-stu-id="18213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18213-107">*lpAddress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18213-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18213-108">字串轉換成的位址指標。</span><span class="sxs-lookup"><span data-stu-id="18213-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="18213-109">*字串* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18213-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18213-110">轉換成位址的字串。</span><span class="sxs-lookup"><span data-stu-id="18213-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18213-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="18213-111">Return value</span></span>

<span data-ttu-id="18213-112">傳回值是轉換後字串的指標。</span><span class="sxs-lookup"><span data-stu-id="18213-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="18213-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="18213-113">Requirements</span></span>



| <span data-ttu-id="18213-114">需求</span><span class="sxs-lookup"><span data-stu-id="18213-114">Requirement</span></span> | <span data-ttu-id="18213-115">值</span><span class="sxs-lookup"><span data-stu-id="18213-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18213-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18213-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18213-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18213-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="18213-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18213-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18213-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18213-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18213-120">標頭</span><span class="sxs-lookup"><span data-stu-id="18213-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="18213-121"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="18213-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="18213-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="18213-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="18213-123"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18213-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="18213-124">DLL</span><span class="sxs-lookup"><span data-stu-id="18213-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18213-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18213-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




