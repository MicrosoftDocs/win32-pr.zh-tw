---
title: Type-Conversion 和封送處理 ACF 屬性
description: 您可以使用這些屬性來控制透過網路傳輸資料的方式。
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL、屬性、類型轉換和封送處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932461"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="05453-104">Type-Conversion 和封送處理 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="05453-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="05453-105">您可以使用這些屬性來控制透過網路傳輸資料的方式。</span><span class="sxs-lookup"><span data-stu-id="05453-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="05453-106">屬性</span><span class="sxs-lookup"><span data-stu-id="05453-106">Attribute</span></span>                                        | <span data-ttu-id="05453-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="05453-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05453-108">[**編碼**](encode.md)[解碼](decode.md)</span><span class="sxs-lookup"><span data-stu-id="05453-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="05453-109">指示 MIDL 針對存根產生的 pickling) 常式公開類型或程式序列化 (。</span><span class="sxs-lookup"><span data-stu-id="05453-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="05453-110">您的用戶端應用程式可以呼叫這些常式，以傳值方式封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="05453-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="05453-111">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="05453-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="05453-112">指定當用戶端資料型別的確切本質對伺服器 (不重要，因為它只需要資料本身，而不是實際的結構) ，或實際用戶端類型在編譯時期是未知的，則會在網路上表示資料類型。</span><span class="sxs-lookup"><span data-stu-id="05453-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="05453-113">例如，如果您的用戶端應用程式使用浮點數的連結清單，您可以將該清單的網路標記法指定為 [**float**](float.md)類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="05453-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="05453-114">**使用者 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="05453-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="05453-115">控制如何藉由執行您自己的封送處理常式，來將資料傳輸到網路上。</span><span class="sxs-lookup"><span data-stu-id="05453-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="05453-116">如果您有 MIDL 未知的資料類型，或您要在位元組由大到小的平臺之間傳遞資訊，這個屬性就很有用。</span><span class="sxs-lookup"><span data-stu-id="05453-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="05453-117">在 [**\_ 行**](in-line.md) 和 [**\_ \_ 行**](out-of-line.md) 中，DCE 封送處理屬性不會在 Microsoft RPC 中執行。</span><span class="sxs-lookup"><span data-stu-id="05453-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="05453-118">MIDL 編譯器會自動將複雜的資料類型封送處理。</span><span class="sxs-lookup"><span data-stu-id="05453-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




