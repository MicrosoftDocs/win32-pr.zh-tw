---
title: async 屬性
description: '\ Async \ ACF 屬性會將遠端程序呼叫定義為非同步作業。'
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- async 屬性 MIDL
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933157"
---
# <a name="async-attribute"></a><span data-ttu-id="1a945-104">async 屬性</span><span class="sxs-lookup"><span data-stu-id="1a945-104">async attribute</span></span>

<span data-ttu-id="1a945-105">\[ **Async** \] ACF 屬性會將遠端程序呼叫定義為非同步作業。</span><span class="sxs-lookup"><span data-stu-id="1a945-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="1a945-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a945-107">*opt-acf-屬性*</span><span class="sxs-lookup"><span data-stu-id="1a945-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="1a945-108">指定選擇性的應用程式設定屬性。</span><span class="sxs-lookup"><span data-stu-id="1a945-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1a945-109">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="1a945-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a945-110">在 IDL 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a945-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="1a945-111">*param 清單*</span><span class="sxs-lookup"><span data-stu-id="1a945-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a945-112">指定選擇性參數清單。</span><span class="sxs-lookup"><span data-stu-id="1a945-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a945-113">備註</span><span class="sxs-lookup"><span data-stu-id="1a945-113">Remarks</span></span>

<span data-ttu-id="1a945-114">此屬性不適用於 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="1a945-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="1a945-115">若要將 RPC 函式宣告為非同步，請先將函數宣告為 IDL 檔案中介面定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="1a945-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="1a945-116">然後藉由套用 async 屬性，在應用程式佈建檔 (ACF) 內修改該函式宣告 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="1a945-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="1a945-117">請注意，函式宣告不會提及非同步控制碼，且系結控制碼為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="1a945-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="1a945-118">\[  \] 在 ACF 檔案中套用 async 屬性會產生適當的程式碼，以便在呼叫此函式時，非同步伺服器預期會在其他參數之前接收非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a945-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="1a945-119">Async 屬性無法搭配 [**/osf**](-osf.md) 命令列參數使用。</span><span class="sxs-lookup"><span data-stu-id="1a945-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1a945-120">範例</span><span class="sxs-lookup"><span data-stu-id="1a945-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="1a945-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a945-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a945-122">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="1a945-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="1a945-123">非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="1a945-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 