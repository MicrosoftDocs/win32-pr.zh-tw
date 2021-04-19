---
title: void 屬性
description: 基底類型 void 表示沒有引數的程式，或未傳回結果值的程式。
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void 屬性 MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106994953"
---
# <a name="void-attribute"></a><span data-ttu-id="0c2d0-104">void 屬性</span><span class="sxs-lookup"><span data-stu-id="0c2d0-104">void attribute</span></span>

<span data-ttu-id="0c2d0-105">基底類型 **void** 表示沒有引數的程式，或未傳回結果值的程式。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="0c2d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c2d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c2d0-107">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="0c2d0-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c2d0-108">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0c2d0-109">*parameter-list*</span><span class="sxs-lookup"><span data-stu-id="0c2d0-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c2d0-110">指定傳遞至函式的參數清單，以及相關聯的參數類型和參數屬性。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0c2d0-111">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="0c2d0-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0c2d0-112">指定函數所傳回之類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="0c2d0-113">*內容-控制碼類型*</span><span class="sxs-lookup"><span data-stu-id="0c2d0-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0c2d0-114">指定採用 **\[** [**內容 \_ 控制碼**](context-handle.md)屬性之類型的名稱 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c2d0-115">備註</span><span class="sxs-lookup"><span data-stu-id="0c2d0-115">Remarks</span></span>

<span data-ttu-id="0c2d0-116">指標類型 **\* void**（以 C 描述可轉換成代表任何指標類型的泛型指標）在 MIDL 中會限制為與 **\[ 內容 \_ 控制碼 \]** 關鍵字搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0c2d0-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="0c2d0-117">範例</span><span class="sxs-lookup"><span data-stu-id="0c2d0-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="0c2d0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c2d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2d0-119">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="0c2d0-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="0c2d0-120">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0c2d0-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="0c2d0-121"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="0c2d0-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




