---
description: GetProtocolFromTable 函式會 \# 根據指定的交付資料表和值，傳回通訊協定&郵件）的控制碼。
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: 'GetProtocolFromTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936617"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="deb3c-103">GetProtocolFromTable 函式</span><span class="sxs-lookup"><span data-stu-id="deb3c-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="deb3c-104">**GetProtocolFromTable** 函數會根據給定的交付資料表和值，傳回通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="deb3c-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb3c-105">語法</span><span class="sxs-lookup"><span data-stu-id="deb3c-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="deb3c-106">參數</span><span class="sxs-lookup"><span data-stu-id="deb3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb3c-107">*hTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="deb3c-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb3c-108">提交資料表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="deb3c-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="deb3c-109">*ItemToFind* \[在\]</span><span class="sxs-lookup"><span data-stu-id="deb3c-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb3c-110">用來在遞交資料表中尋找通訊協定的值。</span><span class="sxs-lookup"><span data-stu-id="deb3c-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="deb3c-111">此值必須可在通訊協定資料中使用。</span><span class="sxs-lookup"><span data-stu-id="deb3c-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="deb3c-112">*lpInstData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="deb3c-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb3c-113">如果可在遞交資料表中使用，則為下一個通訊協定的實例資料。</span><span class="sxs-lookup"><span data-stu-id="deb3c-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="deb3c-114">實例資料的長度不能超過 DWORD \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="deb3c-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb3c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="deb3c-115">Return value</span></span>

<span data-ttu-id="deb3c-116">如果函式成功，則傳回值為通訊協定控制碼。</span><span class="sxs-lookup"><span data-stu-id="deb3c-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="deb3c-117">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="deb3c-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="deb3c-118">備註</span><span class="sxs-lookup"><span data-stu-id="deb3c-118">Remarks</span></span>

<span data-ttu-id="deb3c-119">在執行 [RecognizeFrame](recognizeframe.md) 匯出函式時，會使用 **GetProtocolFromTable** 函數來取得下一個通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="deb3c-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="deb3c-120">如果通訊協定識別接下來的通訊協定，則會呼叫 **GetProtocolFromTable** 函式，以從下一個通訊協定取出控制碼。</span><span class="sxs-lookup"><span data-stu-id="deb3c-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="deb3c-121">**執行個體資料**</span><span class="sxs-lookup"><span data-stu-id="deb3c-121">**Instance data**</span></span>

<span data-ttu-id="deb3c-122">實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。</span><span class="sxs-lookup"><span data-stu-id="deb3c-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb3c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="deb3c-123">Requirements</span></span>



| <span data-ttu-id="deb3c-124">需求</span><span class="sxs-lookup"><span data-stu-id="deb3c-124">Requirement</span></span> | <span data-ttu-id="deb3c-125">值</span><span class="sxs-lookup"><span data-stu-id="deb3c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="deb3c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="deb3c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="deb3c-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deb3c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="deb3c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="deb3c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="deb3c-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deb3c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="deb3c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="deb3c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="deb3c-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="deb3c-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="deb3c-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="deb3c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="deb3c-133"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb3c-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="deb3c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="deb3c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deb3c-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deb3c-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb3c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deb3c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb3c-137">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="deb3c-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




