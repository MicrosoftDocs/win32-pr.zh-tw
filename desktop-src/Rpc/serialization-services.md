---
title: 序列化服務
description: Microsoft RPC 支援兩種編碼和解碼資料的方法，統稱為資料的序列化方式。
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- 遠端程序呼叫 RPC、描述、序列化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675228"
---
# <a name="serialization-services"></a><span data-ttu-id="49380-104">序列化服務</span><span class="sxs-lookup"><span data-stu-id="49380-104">Serialization Services</span></span>

<span data-ttu-id="49380-105">Microsoft RPC 支援兩種編碼和解碼資料的方法，統稱為 *資料* 的序列化方式。</span><span class="sxs-lookup"><span data-stu-id="49380-105">Microsoft RPC supports two methods for encoding and decoding data, collectively called *serializing data*.</span></span> <span data-ttu-id="49380-106">序列化表示資料會從您所控制的緩衝區封送處理和取消封送處理。</span><span class="sxs-lookup"><span data-stu-id="49380-106">Serialization means that the data is marshaled to and unmarshaled from buffers that you control.</span></span> <span data-ttu-id="49380-107">這與傳統的 RPC 使用方式不同，因為存根和 RPC 執行時間程式庫具有封送處理緩衝區的完整控制權，而進程是透明的。</span><span class="sxs-lookup"><span data-stu-id="49380-107">This differs from the traditional usage of RPC, in which the stubs and the RPC run-time library have full control of the marshaling buffers, and the process is transparent.</span></span> <span data-ttu-id="49380-108">您可以使用緩衝區來儲存永久媒體、加密等等。</span><span class="sxs-lookup"><span data-stu-id="49380-108">You can use the buffer for storage on permanent media, encryption, and so on.</span></span> <span data-ttu-id="49380-109">當您編碼資料時，RPC 存根會將資料封送處理至緩衝區，並將緩衝區傳遞給您。</span><span class="sxs-lookup"><span data-stu-id="49380-109">When you encode data, the RPC stubs marshal the data to a buffer and pass the buffer to you.</span></span> <span data-ttu-id="49380-110">當您將資料解碼時，會提供封送處理緩衝區和其中的資料，並將資料從緩衝區取消封送處理至記憶體。</span><span class="sxs-lookup"><span data-stu-id="49380-110">When you decode data, you supply a marshaling buffer with data in it, and the data is unmarshaled from the buffer to memory.</span></span> <span data-ttu-id="49380-111">您可以根據程式或類型來進行序列化。</span><span class="sxs-lookup"><span data-stu-id="49380-111">You can serialize on a procedure or type basis.</span></span>

> [!Note]  
> <span data-ttu-id="49380-112">*Pickling* 一詞通常是在開發人員用來描述序列化。</span><span class="sxs-lookup"><span data-stu-id="49380-112">The term *pickling* is commonly used among developers to describe serialization.</span></span> <span data-ttu-id="49380-113">事實上，Windows SDK 範例包含名為 *pickle* 的目錄，它會保留 RPC 序列化範例程式。</span><span class="sxs-lookup"><span data-stu-id="49380-113">In fact, the Windows SDK samples contains a directory called *pickle* that preserves the RPC serialization sample programs.</span></span>

 

<span data-ttu-id="49380-114">針對其他用途，序列化會利用 RPC 機制來封送處理和封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="49380-114">Serialization leverages the RPC mechanisms for marshaling and unmarshaling data for other purposes.</span></span> <span data-ttu-id="49380-115">例如，應用程式可以將不同類型的數個物件序列化為緩衝區，然後在單一作業中寫入整個緩衝區，而不是使用數個 i/o 作業將物件群組序列化為數據流。</span><span class="sxs-lookup"><span data-stu-id="49380-115">For example, instead of using several I/O operations to serialize a group of objects to a stream, an application can optimize performance by serializing several objects of different types into a buffer and then writing the entire buffer in a single operation.</span></span> <span data-ttu-id="49380-116">操作序列化控制碼的函式與您所使用的序列化類型無關。</span><span class="sxs-lookup"><span data-stu-id="49380-116">The functions that manipulate serialization handles are independent of the type of serialization you are using.</span></span>

<span data-ttu-id="49380-117">另一個範例是，如果您需要使用 RPC 以外的網路傳輸機制，例如 Microsoft Windows 通訊端 (Winsock) 。</span><span class="sxs-lookup"><span data-stu-id="49380-117">As another example, if you need to use a network transport mechanism besides RPC, such as Microsoft Windows Sockets (Winsock).</span></span> <span data-ttu-id="49380-118">使用 RPC 序列化時，您的程式可以呼叫函式，將您的資料封送處理為緩衝區，然後使用 Winsock 傳輸此資料。</span><span class="sxs-lookup"><span data-stu-id="49380-118">With RPC serialization, your program can make calls to functions that marshal your data into buffers and then transmit this data using Winsock.</span></span> <span data-ttu-id="49380-119">當您的應用程式接收資料時，可以使用 RPC 序列化機制，從 Winsock 常式所填滿的緩衝區 unmarshal 資料。</span><span class="sxs-lookup"><span data-stu-id="49380-119">When your application receives data, it can use the RPC serialization mechanism to unmarshal data from buffers filled by the Winsock routines.</span></span> <span data-ttu-id="49380-120">這可為您提供 RPC 樣式應用程式的許多優點，同時也可讓您使用非 RPC 傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="49380-120">This provides you with many of the advantages of RPC-style applications, and at the same time, it enables you to use non-RPC transport mechanisms.</span></span>

<span data-ttu-id="49380-121">您也可以使用序列化進行與網路通訊無關的用途。</span><span class="sxs-lookup"><span data-stu-id="49380-121">You can also use serialization for purposes unrelated to network communications.</span></span> <span data-ttu-id="49380-122">例如，當您使用 RPC 編碼函式將資料封送處理至緩衝區時，就可以將它儲存在檔案中，供其他應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="49380-122">For example, once you use the RPC encoding functions to marshal data to a buffer, you can store it in a file for use by another application.</span></span> <span data-ttu-id="49380-123">您也可以將它加密。</span><span class="sxs-lookup"><span data-stu-id="49380-123">You can also encrypt it.</span></span> <span data-ttu-id="49380-124">您甚至可以使用它，在資料庫中儲存與硬體和作業系統無關的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="49380-124">You can even use it to store a hardware- and operating system-independent representation of data in a database.</span></span>

<span data-ttu-id="49380-125">下列主題提供 Microsoft RPC 支援的序列化服務討論：</span><span class="sxs-lookup"><span data-stu-id="49380-125">The following topics present a discussion of the serialization services that Microsoft RPC supports:</span></span>

-   [<span data-ttu-id="49380-126">使用序列化服務</span><span class="sxs-lookup"><span data-stu-id="49380-126">Using Serialization Services</span></span>](using-serialization-services.md)
-   [<span data-ttu-id="49380-127">程式序列化</span><span class="sxs-lookup"><span data-stu-id="49380-127">Procedure Serialization</span></span>](procedure-serialization.md)
-   [<span data-ttu-id="49380-128">類型序列化</span><span class="sxs-lookup"><span data-stu-id="49380-128">Type Serialization</span></span>](type-serialization.md)
-   [<span data-ttu-id="49380-129">序列化控制碼</span><span class="sxs-lookup"><span data-stu-id="49380-129">Serialization Handles</span></span>](serialization-handles.md)

 

 




