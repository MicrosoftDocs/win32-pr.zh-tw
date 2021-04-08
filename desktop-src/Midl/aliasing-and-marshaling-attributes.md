---
title: 別名和封送處理屬性
description: 分散式應用程式在呼叫介面程式時，幾乎一律會在用戶端和伺服器程式之間傳遞資料。
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL、屬性 MIDL、別名和封送處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022029"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="98484-104">別名和封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="98484-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="98484-105">分散式應用程式在呼叫介面程式時，幾乎一律會在用戶端和伺服器程式之間傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="98484-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="98484-106">開發人員會使用 MIDL 來描述用戶端和伺服器程式以標準方式傳遞的資料。</span><span class="sxs-lookup"><span data-stu-id="98484-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="98484-107">MIDL 編譯器會針對用戶端和伺服器建立應用程式 stub 或 proxy，以將資料轉換成可透過網路傳送的標準化格式。</span><span class="sxs-lookup"><span data-stu-id="98484-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="98484-108">這種格式（ (NDR) 格式的網路資料表示）通常稱為資料的電傳格式。</span><span class="sxs-lookup"><span data-stu-id="98484-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="98484-109">存根必須將其原生格式的資料從程式的記憶體空間轉換成 NDR。</span><span class="sxs-lookup"><span data-stu-id="98484-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="98484-110">這項轉換稱為封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="98484-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="98484-111">當用戶端或伺服器程式接收資料時，它必須將該程式的資料從 NDR 轉換成原生格式。</span><span class="sxs-lookup"><span data-stu-id="98484-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="98484-112">這稱為將資料解除封送。</span><span class="sxs-lookup"><span data-stu-id="98484-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="98484-113">使用別名和封送處理屬性來控制如何將資料封裝成 NDR 格式，並透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="98484-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="98484-114">屬性</span><span class="sxs-lookup"><span data-stu-id="98484-114">Attribute</span></span>                             | <span data-ttu-id="98484-115">使用方式</span><span class="sxs-lookup"><span data-stu-id="98484-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98484-116">**呼叫 \_ as**</span><span class="sxs-lookup"><span data-stu-id="98484-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="98484-117">將不可遠端處理函數對應至遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="98484-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="98484-118">**iid \_ 為**</span><span class="sxs-lookup"><span data-stu-id="98484-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="98484-119">提供 COM 介面的介面識別碼，該介面是指標的物件。</span><span class="sxs-lookup"><span data-stu-id="98484-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="98484-120">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="98484-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="98484-121">將資料類型轉換成更簡單的類型，以便透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="98484-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="98484-122">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="98484-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="98484-123">類似于 [**傳送 \_ as**](transmit-as.md) ，但您會執行常式來調整大小、封送處理、unmarshal 和釋放資料。</span><span class="sxs-lookup"><span data-stu-id="98484-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="98484-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="98484-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98484-125">類型轉換和封送處理 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="98484-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




