---
title: disable_consistency_check 屬性
description: 指示 RPC 不要強制執行相互關聯一致性檢查。
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300403"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="b6a74-103">停用 \_ 一致性 \_ 檢查屬性</span><span class="sxs-lookup"><span data-stu-id="b6a74-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="b6a74-104">指示 RPC 不要強制執行相互關聯一致性檢查。</span><span class="sxs-lookup"><span data-stu-id="b6a74-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="b6a74-105">針對相互關聯的參數，RPC 會強制在相互關聯計數變數為非 null 時傳遞非 null 的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b6a74-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="b6a74-106">範例</span><span class="sxs-lookup"><span data-stu-id="b6a74-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="b6a74-107">如果 *MyString* 為 **Null**，RPC 將會拒絕呼叫，除非 Length 設定為0。</span><span class="sxs-lookup"><span data-stu-id="b6a74-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="b6a74-108">請注意，當 *MyString* 為非 Null 時，rpc 將允許 *長度* 為0，而 rpc 會將 *MyString* 視為0長度的緩衝區配置。</span><span class="sxs-lookup"><span data-stu-id="b6a74-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a74-109">備註</span><span class="sxs-lookup"><span data-stu-id="b6a74-109">Remarks</span></span>

<span data-ttu-id="b6a74-110">若要停用這種檢查，IDL 可以 \[ \_ \_ \] 在參數、typedef 或指標類型上包含停用一致性檢查屬性。</span><span class="sxs-lookup"><span data-stu-id="b6a74-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="b6a74-111">這會將 RPC 導向，使其不會強制執行參數或指標所指向之緩衝區的緩衝區指標和相互關聯變數之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="b6a74-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="b6a74-112">若要停用整個 MIDL 編譯 (的一致性檢查，並在所有情況下停用強制檢查) ，可以使用 MIDL 命令列參數 [/backward \_ 相容性 maybenull \_ sizeis](-backward-compat.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6a74-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="b6a74-113">這需要 MIDL 編譯的目標至少為 "target NT60"。</span><span class="sxs-lookup"><span data-stu-id="b6a74-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




