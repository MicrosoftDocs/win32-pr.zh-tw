---
description: CreatePropertyDatabase 函數會建立一個屬性資料庫來儲存通訊協定的屬性。
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: 'CreatePropertyDatabase 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974661"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="f47d4-103">CreatePropertyDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="f47d4-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="f47d4-104">**CreatePropertyDatabase** 函數會建立一個屬性資料庫來儲存通訊協定的屬性。</span><span class="sxs-lookup"><span data-stu-id="f47d4-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f47d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="f47d4-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="f47d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="f47d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47d4-107">*hProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f47d4-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47d4-108">與資料庫相關聯之通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f47d4-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="f47d4-109">當網路監視器呼叫 [Register](register-parser.md) 函數時，網路監視器會將通訊協定控制碼傳遞給剖析器 DLL。</span><span class="sxs-lookup"><span data-stu-id="f47d4-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="f47d4-110">*nProperties* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f47d4-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47d4-111">儲存在資料庫中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="f47d4-111">Number of properties stored in the database.</span></span> <span data-ttu-id="f47d4-112">將此參數設定為通訊協定支援的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="f47d4-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47d4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f47d4-113">Return value</span></span>

<span data-ttu-id="f47d4-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="f47d4-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f47d4-115">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f47d4-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="f47d4-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f47d4-116">Return code</span></span>                                                                                             | <span data-ttu-id="f47d4-117">Description</span><span class="sxs-lookup"><span data-stu-id="f47d4-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f47d4-118"><dt>**NMERR \_ 內部 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="f47d4-119">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="f47d4-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f47d4-120"><dt>**NMERR \_ 不正確 \_ HPOTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="f47d4-121">*HProtocol* 中指定之通訊協定的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="f47d4-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="f47d4-122"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="f47d4-123">網路監視器沒有足夠的記憶體來建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="f47d4-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f47d4-124">備註</span><span class="sxs-lookup"><span data-stu-id="f47d4-124">Remarks</span></span>

<span data-ttu-id="f47d4-125">只有在執行 [Register](register-parser.md)函數時，才應該呼叫 **CreatePropertyDatabase** 函數。</span><span class="sxs-lookup"><span data-stu-id="f47d4-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="f47d4-126">剖析器會使用 **CreatePropertyDatabase** 來建立描述通訊協定屬性的屬性資料庫。</span><span class="sxs-lookup"><span data-stu-id="f47d4-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="f47d4-127">網路監視器會使用資料庫來解讀通訊協定內的資訊。</span><span class="sxs-lookup"><span data-stu-id="f47d4-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="f47d4-128">**CreatePropertyDatabase** 函數會配置網路監視器需要維護屬性資料庫的結構。</span><span class="sxs-lookup"><span data-stu-id="f47d4-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47d4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f47d4-129">Requirements</span></span>



| <span data-ttu-id="f47d4-130">需求</span><span class="sxs-lookup"><span data-stu-id="f47d4-130">Requirement</span></span> | <span data-ttu-id="f47d4-131">值</span><span class="sxs-lookup"><span data-stu-id="f47d4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f47d4-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f47d4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f47d4-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f47d4-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f47d4-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f47d4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f47d4-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f47d4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f47d4-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f47d4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f47d4-137"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f47d4-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="f47d4-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f47d4-139"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f47d4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f47d4-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f47d4-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f47d4-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47d4-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f47d4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47d4-143">註冊</span><span class="sxs-lookup"><span data-stu-id="f47d4-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




