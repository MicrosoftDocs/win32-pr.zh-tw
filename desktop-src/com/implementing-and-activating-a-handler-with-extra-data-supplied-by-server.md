---
title: 使用伺服器提供的額外資料來執行和啟用處理常式
description: 使用伺服器提供的額外資料來執行和啟用處理常式
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104321323"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a><span data-ttu-id="847e0-103">使用伺服器提供的額外資料來執行和啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="847e0-103">Implementing and Activating a Handler with Extra Data Supplied by Server</span></span>

<span data-ttu-id="847e0-104">如果伺服器要在封包中包含一些額外的資料以供處理常式使用，則伺服器必須同時執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) 和 [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="847e0-104">If the server wants to include some extra data in the packet for the handler to use, the server must implement both the [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) and the [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) interfaces.</span></span> <span data-ttu-id="847e0-105">伺服器必須匯總標準封送處理器，而且必須將封送處理的第一個部分委派給匯總的標準封送處理器（包括 [**IMarshal：： GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass)），而且必須將它自己的資料大小加入標準封送處理器的 [**IMarshal：： GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)傳回的大小。</span><span class="sxs-lookup"><span data-stu-id="847e0-105">The server must aggregate the standard marshaler and must delegate the first part of the marshaling to the aggregated standard marshaler, including [**IMarshal::GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), and must add its own data size to the size returned by the standard marshaler's [**IMarshal::GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax).</span></span> <span data-ttu-id="847e0-106">標準封送處理器會呼叫 [**IStdMarshalInfo：： GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) 來取得要建立之處理常式的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="847e0-106">The standard marshaler calls [**IStdMarshalInfo::GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) to get the CLSID of the handler to be created.</span></span> <span data-ttu-id="847e0-107">標準封送處理器完成封送處理之後，伺服器會將自己的額外資料寫入資料流程中。</span><span class="sxs-lookup"><span data-stu-id="847e0-107">After the standard marshaler has done its marshaling, the server then writes its own extra data into the stream.</span></span> <span data-ttu-id="847e0-108">下圖顯示產生的結構以及資料流程中的額外資料，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="847e0-108">The resulting structures, with extra data in the stream, are shown in the following illustration:</span></span>

![顯示資料流程中有額外資料之結構的圖表。](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a><span data-ttu-id="847e0-110">資料流程中具有額外資料的 Server-Side 結構</span><span class="sxs-lookup"><span data-stu-id="847e0-110">Server-Side Structures with Extra Data in Stream</span></span>

<span data-ttu-id="847e0-111">如此一來，如果無法建立處理常式，則在用戶端上呼叫 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 時，可以略過任何未讀取的資料，並將資料流程保留在適當的位置。</span><span class="sxs-lookup"><span data-stu-id="847e0-111">This allows the call from COM to [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) on the client side the ability to skip over any unread data and leave the stream in the appropriate position following all the marshaled interface data if the handler cannot be created.</span></span>

## <a name="client-side-structures-with-extra-data-in-stream"></a><span data-ttu-id="847e0-112">資料流程中具有額外資料的 Client-Side 結構</span><span class="sxs-lookup"><span data-stu-id="847e0-112">Client-Side Structures with Extra Data in Stream</span></span>

<span data-ttu-id="847e0-113">在資料流程中沒有額外的伺服器資料的情況下，用戶端對 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 的 COM 呼叫將會建立身分識別和處理常式。</span><span class="sxs-lookup"><span data-stu-id="847e0-113">As in the case where there is no extra server data in the stream, the client-side COM call to [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) will create the identity and handler.</span></span> <span data-ttu-id="847e0-114">處理常式必須執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，而且必須先將 **IMarshal** 呼叫委派給匯總的標準封送處理器，然後封送處理或 unmarshal 伺服器提供的任何額外資料。</span><span class="sxs-lookup"><span data-stu-id="847e0-114">The handler must implement [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) and must delegate the **IMarshal** calls to the aggregated standard marshaler first and then marshal or unmarshal any extra data that the server provided.</span></span> <span data-ttu-id="847e0-115">將會針對每個 unmarshal 呼叫處理常式的 [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) ，不論它是否已將介面取消封送處理。</span><span class="sxs-lookup"><span data-stu-id="847e0-115">The handler's [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) will be called for every unmarshal, regardless of whether it has unmarshaled the interface before or not.</span></span> <span data-ttu-id="847e0-116">在此情況下，伺服器不會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) ，但處理常式必須是。</span><span class="sxs-lookup"><span data-stu-id="847e0-116">In this case, the server does not call [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) but the handler must.</span></span> <span data-ttu-id="847e0-117">產生的用戶端結構如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="847e0-117">The resulting client-side structure is shown in the following illustration.</span></span>

![顯示用戶端結構的圖表。](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a><span data-ttu-id="847e0-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="847e0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847e0-120">輕量 Client-Side 處理常式</span><span class="sxs-lookup"><span data-stu-id="847e0-120">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 