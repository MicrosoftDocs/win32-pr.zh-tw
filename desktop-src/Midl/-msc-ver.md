---
title: /msc_ver 參數
description: /Msc \_ ver 參數是用來允許 MIDL 產生程式碼，其中包含不同版本的 Microsoft C/c + + 編譯器的優化。
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841428"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="71b3f-104">/msc \_ ver 參數</span><span class="sxs-lookup"><span data-stu-id="71b3f-104">/msc\_ver switch</span></span>

<span data-ttu-id="71b3f-105">**/Msc \_ ver** 參數是用來允許 MIDL 產生程式碼，其中包含不同版本的 Microsoft C/c + + 編譯器的優化。</span><span class="sxs-lookup"><span data-stu-id="71b3f-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="71b3f-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="71b3f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="71b3f-107">*版本 \_ 號碼*</span><span class="sxs-lookup"><span data-stu-id="71b3f-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="71b3f-108">指定將用來編譯分散式應用程式之用戶端和伺服器存根的 Microsoft Visual C++ 編譯器的整數版本號碼。</span><span class="sxs-lookup"><span data-stu-id="71b3f-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="71b3f-109">預設版本號碼是1100，對應至 Visual C++ 版本5.0。</span><span class="sxs-lookup"><span data-stu-id="71b3f-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="71b3f-110">版本號碼1200對應于 Visual C++ 版本6.0，依此類推。</span><span class="sxs-lookup"><span data-stu-id="71b3f-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71b3f-111">備註</span><span class="sxs-lookup"><span data-stu-id="71b3f-111">Remarks</span></span>

<span data-ttu-id="71b3f-112">特別是，1100或更高版本的版本值會導致 MIDL 編譯器使用 **\_ \_ declspec (uuid () )** 指示詞來產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="71b3f-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="71b3f-113">它也會啟用使用 **\_ \_ declspec (selectany)** 和 **\_ \_ declspec (novtable)** 指示詞的宏。</span><span class="sxs-lookup"><span data-stu-id="71b3f-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




