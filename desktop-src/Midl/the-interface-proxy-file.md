---
title: 介面 Proxy 檔案
description: 介面 proxy 檔案 (U \_ p. c) 是 c 檔案，其中包含的常式相當於用戶端 stub 中的常式和物件 (COM) 介面中的伺服器 stub 檔案。
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL 和 COM MIDL、介面、proxy 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932401"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="6e9e1-104">介面 Proxy 檔案</span><span class="sxs-lookup"><span data-stu-id="6e9e1-104">The Interface Proxy File</span></span>

<span data-ttu-id="6e9e1-105">介面 proxy 檔案 (U \_ p. c) 是 c 檔案，其中包含的常式相當於用戶端 stub 中的常式和物件 (COM) 介面中的伺服器 stub 檔案。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="6e9e1-106">這個檔案包含在編譯器的內嵌模式中，用戶端和伺服器的代理常式的執行方式，或在解讀模式中的對等資料和 Thunk，以及其他適當的 COM 粘附資料（例如 proxy 和存根 Vtable）。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="6e9e1-107">介面 proxy 檔案僅包含目前 IDL 檔案中所定義介面之方法的支援常式和資料。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="6e9e1-108">若要明確說明這種行為，請在本節中使用擴充的範例。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="6e9e1-109">當編譯具有繼承自 IFaceA 之介面（例如 IFaceB）的 IDL 檔案時，會將 IFaceB 相關的輔助資料和常式產生至目前的 proxy 檔案，而基底介面 IFaceA 相關輔助資料和常式則是在包含 IFaceA 定義的 IDL 檔案所產生的 proxy 中找到。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="6e9e1-110">編譯器會產生識別基底介面之代理程式的所有必要資料，並在需要時將其委派給它們，以支援透過 IFaceB 介面所使用的 IFaceA 方法。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="6e9e1-111">針對目前 IDL 檔案中介面內的每個方法，在混合模式中編譯時，proxy 檔案會包含下列兩個代理方法 ([/os](-os.md)) ，而在解譯器模式中編譯時則對等解譯器資料 ([/Oi](-oi.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="6e9e1-112">用戶端代理，例如 \_ \_ 此範例中的 IFaceB 方法 Proxy。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="6e9e1-113">此用戶端代理是用戶端（例如 IFaceB：： Method）分派的虛擬進入點。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="6e9e1-114">它會將輸入引數封送處理成可形式、將封送處理的引數連同識別介面和作業的資訊一起傳送，然後在叫用的作業傳回時，拆收傳回值和任何輸出引數。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="6e9e1-115">伺服器端代理，例如 IFaceB \_ 方法 \_ Stub。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="6e9e1-116">此伺服器端代理是基礎執行時間在伺服器上分派給的虛擬進入點，用以模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="6e9e1-117">它會拆收輸入引數以複寫用戶端資料、叫用伺服器的介面函式執行，然後將傳回值和任何輸出引數封送處理並傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="6e9e1-118">從檔案產生之 proxy 檔案的預設名稱。 .idl 是 file \_ p. c. 使用 [**/proxy**](-proxy.md) MIDL 編譯器參數覆寫介面 proxy 檔案的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="6e9e1-119">[**/Env**](-env.md)和 [**/out**](-out.md)參數會影響這個檔案。</span><span class="sxs-lookup"><span data-stu-id="6e9e1-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




