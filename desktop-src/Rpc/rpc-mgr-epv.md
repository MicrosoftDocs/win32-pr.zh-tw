---
title: 'RPC_MGR_EPV (Rpcdce) '
description: 資料類型 RPC \_ MGR \_ EPV 定義了管理員進入點向量。
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685586"
---
# <a name="rpc_mgr_epv"></a><span data-ttu-id="59359-104">RPC \_ MGR \_ EPV</span><span class="sxs-lookup"><span data-stu-id="59359-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="59359-105">資料類型 **RPC \_ MGR \_ EPV** 定義了管理員進入點向量。</span><span class="sxs-lookup"><span data-stu-id="59359-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="59359-106">成員</span><span class="sxs-lookup"><span data-stu-id="59359-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="59359-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span><span class="sxs-lookup"><span data-stu-id="59359-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="59359-108">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="59359-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="59359-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**傳回類型**</span><span class="sxs-lookup"><span data-stu-id="59359-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="59359-110">指定 IDL 檔案中指出的函式 **Functionname** 所傳回的類型。</span><span class="sxs-lookup"><span data-stu-id="59359-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="59359-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span><span class="sxs-lookup"><span data-stu-id="59359-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="59359-112">指定 IDL 檔案中指出的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="59359-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="59359-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param 清單**</span><span class="sxs-lookup"><span data-stu-id="59359-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="59359-114">針對 IDL 檔案中的函式 **Functionname** 指定指定的參數。</span><span class="sxs-lookup"><span data-stu-id="59359-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59359-115">備註</span><span class="sxs-lookup"><span data-stu-id="59359-115">Remarks</span></span>

<span data-ttu-id="59359-116"> (EPV) 的 manager 進入點向量是函式指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="59359-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="59359-117">陣列包含 IDL 檔案中指定之函式的實作為指標。</span><span class="sxs-lookup"><span data-stu-id="59359-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="59359-118">陣列中的元素數目會設定為 IDL 檔案中指定的函數數目。</span><span class="sxs-lookup"><span data-stu-id="59359-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="59359-119">應用程式也可以有多個 EPVs，表示介面中指定之函式的多個實作為。</span><span class="sxs-lookup"><span data-stu-id="59359-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="59359-120">MIDL 編譯器會產生名為 \* if-name \***\_ SERVER \_ EPV** 的預設 **EPV** 資料類型，其中 *if-name* 會在 IDL 檔案中指定介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="59359-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="59359-121">MIDL 編譯器會初始化此預設 **EPV** ，以包含 IDL 檔案中所指定之每個程式的函式指標。</span><span class="sxs-lookup"><span data-stu-id="59359-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="59359-122">當伺服器提供相同介面的多個型別時，伺服器應用程式必須針對每個介面的執行，宣告和初始化一個類型的變數（ \*如果-name \* \* \* \_ server \_ EPV\*\*）。</span><span class="sxs-lookup"><span data-stu-id="59359-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="59359-123">每個 **EPV** 都必須針對 IDL 檔案中定義的每個程式，各包含一個進入點 (函式指標) 。</span><span class="sxs-lookup"><span data-stu-id="59359-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="59359-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="59359-124">Requirements</span></span>



| <span data-ttu-id="59359-125">需求</span><span class="sxs-lookup"><span data-stu-id="59359-125">Requirement</span></span> | <span data-ttu-id="59359-126">值</span><span class="sxs-lookup"><span data-stu-id="59359-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59359-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59359-127">Minimum supported client</span></span><br/> | <span data-ttu-id="59359-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59359-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="59359-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59359-129">Minimum supported server</span></span><br/> | <span data-ttu-id="59359-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59359-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59359-131">標頭</span><span class="sxs-lookup"><span data-stu-id="59359-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="59359-132"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="59359-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59359-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59359-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59359-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="59359-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="59359-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="59359-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="59359-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="59359-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="59359-137">**RpcServerUnregisterIf**</span><span class="sxs-lookup"><span data-stu-id="59359-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="59359-138">**RpcServerUnregisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="59359-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





