---
title: notify_flag 屬性
description: '\ 通知 \_ 旗標 \ 屬性會提供通知，指出是否呼叫伺服器常式。'
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag 屬性 MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022300"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="77d91-104">通知 \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="77d91-104">notify\_flag attribute</span></span>

<span data-ttu-id="77d91-105">**\[ 通知 \_ 旗 \]** 標屬性會提供通知，指出是否呼叫伺服器常式。</span><span class="sxs-lookup"><span data-stu-id="77d91-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="77d91-106">參數</span><span class="sxs-lookup"><span data-stu-id="77d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d91-107">*程式-名稱*</span><span class="sxs-lookup"><span data-stu-id="77d91-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="77d91-108">與通知 \_ 旗標程式相關聯的遠端程式名稱。</span><span class="sxs-lookup"><span data-stu-id="77d91-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77d91-109">備註</span><span class="sxs-lookup"><span data-stu-id="77d91-109">Remarks</span></span>

<span data-ttu-id="77d91-110">**\[ 通知 \_ 旗 \]** 標屬性類似于 [ **\[ 通知 \]** ] 屬性的使用方式。</span><span class="sxs-lookup"><span data-stu-id="77d91-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="77d91-111">[ **\[ 通知 \_ 旗 \]** 標程式名稱] 是以 [ **\_ 通知] \_ 旗** 標做為尾碼的遠端程式名稱。</span><span class="sxs-lookup"><span data-stu-id="77d91-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="77d91-112">**\_ 通知 \_ 旗** 標程式不需要任何參數，也不會傳回結果。</span><span class="sxs-lookup"><span data-stu-id="77d91-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="77d91-113">這項程式的原型也會在標頭檔中產生。</span><span class="sxs-lookup"><span data-stu-id="77d91-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="77d91-114">例如，如果 IDL 檔案包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="77d91-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="77d91-115">在 ACF for MIDL 中指定下列各項，以產生 **\_ 通知 \_ 旗** 標呼叫：</span><span class="sxs-lookup"><span data-stu-id="77d91-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="77d91-116">MIDL 編譯器將會產生包含下列 **\_ 通知 \_ 旗** 標程式呼叫的伺服器 stub 程式碼：</span><span class="sxs-lookup"><span data-stu-id="77d91-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="77d91-117">標頭檔將包含原型：</span><span class="sxs-lookup"><span data-stu-id="77d91-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="77d91-118">如果呼叫伺服器常式， **\_ MIDL \_ NotifyFlag** 為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="77d91-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="77d91-119">範例</span><span class="sxs-lookup"><span data-stu-id="77d91-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="77d91-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77d91-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d91-121">**通知**</span><span class="sxs-lookup"><span data-stu-id="77d91-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




