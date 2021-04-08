---
title: 使用者封送處理
description: 遠端程序呼叫中的使用者封送處理 (RPC) 。
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840024"
---
# <a name="user-marshal"></a><span data-ttu-id="3843b-103">使用者封送處理</span><span class="sxs-lookup"><span data-stu-id="3843b-103">User-marshal</span></span>

<span data-ttu-id="3843b-104">使用者封送處理的格式字串類似于傳輸 \_ 方式：</span><span class="sxs-lookup"><span data-stu-id="3843b-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="3843b-105">旗標<1> 位元組包含上方旗標半形和較低的對齊半形。</span><span class="sxs-lookup"><span data-stu-id="3843b-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="3843b-106">旗標半形的上方2位可用來描述網路類型是否定義為唯一指標、參考指標或沒有指標 (不能是 ptr) 。</span><span class="sxs-lookup"><span data-stu-id="3843b-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="3843b-107">下列資訊清單已定義為可設定/取得旗標：</span><span class="sxs-lookup"><span data-stu-id="3843b-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="3843b-108">旗標字組的對齊半位，可保持傳輸類型的對齊。</span><span class="sxs-lookup"><span data-stu-id="3843b-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="3843b-109">四 \_ 個索引<2> 是使用者封送處理函式的回呼常式最四個索引。</span><span class="sxs-lookup"><span data-stu-id="3843b-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="3843b-110">常式位置如下：調整、封送處理、封送處理和釋放常式。</span><span class="sxs-lookup"><span data-stu-id="3843b-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="3843b-111">使用者 \_ 類型 \_ 記憶體 \_ 大小<2> 提供使用者特定類型的大小，包括未知的類型。</span><span class="sxs-lookup"><span data-stu-id="3843b-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="3843b-112">\_ \_ \_ 當大小變化或實際的固定大小時，傳輸的類型緩衝區大小<2> 為零。</span><span class="sxs-lookup"><span data-stu-id="3843b-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="3843b-113">這是一項優化，可讓 MIDL 在調整緩衝區大小時略過回呼，也可在釋放時略過回呼。</span><span class="sxs-lookup"><span data-stu-id="3843b-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="3843b-114">範圍</span><span class="sxs-lookup"><span data-stu-id="3843b-114">Range</span></span>

<span data-ttu-id="3843b-115">\[範圍 \] 檢查可提供其他方法來驗證 NDR 層的引數。</span><span class="sxs-lookup"><span data-stu-id="3843b-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="3843b-116">\[範圍描述項的 \] 格式如下：</span><span class="sxs-lookup"><span data-stu-id="3843b-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="3843b-117">旗標採用上半個位元組，而類型為第二個位元組的下半部半形。</span><span class="sxs-lookup"><span data-stu-id="3843b-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="3843b-118">低和高值取決於要檢查的變數類型。</span><span class="sxs-lookup"><span data-stu-id="3843b-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="3843b-119">旗標旨在作為擴充車輛;編譯器已將半值設定為零。</span><span class="sxs-lookup"><span data-stu-id="3843b-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




