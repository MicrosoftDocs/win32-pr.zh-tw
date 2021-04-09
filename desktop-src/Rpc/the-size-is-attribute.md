---
title: Size_is 屬性
description: '\ 的大小 \_ 為 \ 屬性，與指定陣列配置大小的整數常數、運算式或變數相關聯。'
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842400"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="683c7-104">\[大小 \_ 為 \] Attribute</span><span class="sxs-lookup"><span data-stu-id="683c7-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="683c7-105">\[ [Size \_ 是](/windows/desktop/Midl/size-is) \] 與指定陣列配置大小的整數常數、運算式或變數相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="683c7-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="683c7-106">請考慮長度由使用者輸入決定的字元陣列：</span><span class="sxs-lookup"><span data-stu-id="683c7-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="683c7-107">\*標示變數陣列維度之預留位置的星號 () 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="683c7-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="683c7-108">伺服器 stub 必須在伺服器上配置對應至該參數之用戶端記憶體的記憶體。</span><span class="sxs-lookup"><span data-stu-id="683c7-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="683c7-109">指定大小的變數必須一律至少為 \[ [in](/windows/desktop/Midl/in) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="683c7-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="683c7-110">需要 **\[ in \]** 方向屬性，以便在進入伺服器 stub 時定義大小值。</span><span class="sxs-lookup"><span data-stu-id="683c7-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="683c7-111">此大小值提供伺服器 stub 配置記憶體所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="683c7-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="683c7-112">Size 參數也可以是 \[ in、 [out](/windows/desktop/Midl/out-idl) \] 。</span><span class="sxs-lookup"><span data-stu-id="683c7-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="683c7-113">比方說，如果用戶端傳送的陣列不足以容納伺服器需要儲存的資料，這就很有用。</span><span class="sxs-lookup"><span data-stu-id="683c7-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="683c7-114">您可以使用 **\[ in、out \]** size 參數將所需的大小傳送回用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="683c7-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="683c7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="683c7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="683c7-116">多個指標層級</span><span class="sxs-lookup"><span data-stu-id="683c7-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 