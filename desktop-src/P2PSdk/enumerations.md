---
title: " (對等基礎結構) 的列舉"
description: 藉由使用列舉，您可以取得符合準則的所有特定對等實體清單。
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993139"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="1a810-103"> (對等基礎結構) 的列舉</span><span class="sxs-lookup"><span data-stu-id="1a810-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="1a810-104">藉由使用列舉，您可以取得符合準則的所有特定對等實體清單。</span><span class="sxs-lookup"><span data-stu-id="1a810-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="1a810-105">**取得列舉並取得結果**</span><span class="sxs-lookup"><span data-stu-id="1a810-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="1a810-106">取得列舉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a810-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="1a810-107">呼叫 **PeerEnum** 函式，例如，呼叫 [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) 對等圖形函數。</span><span class="sxs-lookup"><span data-stu-id="1a810-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="1a810-108">**PeerEnum** 函式會建立列舉，並將該列舉的控制碼傳回給呼叫應用程式。</span><span class="sxs-lookup"><span data-stu-id="1a810-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="1a810-109">您必須使用這個控制碼來取得結果。</span><span class="sxs-lookup"><span data-stu-id="1a810-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="1a810-110">（選擇性）取得列舉中的實體數目。</span><span class="sxs-lookup"><span data-stu-id="1a810-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="1a810-111">呼叫 **GetItemCount** 函數，例如，呼叫 [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) 或 [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)。</span><span class="sxs-lookup"><span data-stu-id="1a810-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a810-112">您可以使用 **GetItemCount** 函式所傳回的值來判斷可供取出的專案數目。</span><span class="sxs-lookup"><span data-stu-id="1a810-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="1a810-113">取出結果群組。</span><span class="sxs-lookup"><span data-stu-id="1a810-113">Retrieve a group of results.</span></span> <span data-ttu-id="1a810-114">呼叫 **GetNextItem** 函數，例如，呼叫 [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)。</span><span class="sxs-lookup"><span data-stu-id="1a810-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a810-115">當應用程式呼叫 **GetNextItem** 函式時，它會指定要傳回的實體數目，然後函式會傳回實體指標陣列的指標，以及實體數目（永遠小於或等於指定的數目）。</span><span class="sxs-lookup"><span data-stu-id="1a810-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="1a810-116">應用程式可能需要多次呼叫此函數，直到傳回的實體數目小於要求的數目。</span><span class="sxs-lookup"><span data-stu-id="1a810-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="1a810-117">不需要資料之後，請釋放資料的指標。</span><span class="sxs-lookup"><span data-stu-id="1a810-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="1a810-118">呼叫 **FreeData** 函數，例如，呼叫 [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) 或 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)。</span><span class="sxs-lookup"><span data-stu-id="1a810-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a810-119">如需詳細資訊，請參閱 [釋放對等資料](freeing-peer-data.md)。</span><span class="sxs-lookup"><span data-stu-id="1a810-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="1a810-120">應用程式不需要列舉的控制碼之後，請加以釋放。</span><span class="sxs-lookup"><span data-stu-id="1a810-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="1a810-121">呼叫 **EndEnumeration** 函數，例如，呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) 或 [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)。</span><span class="sxs-lookup"><span data-stu-id="1a810-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="1a810-122">列舉的範例</span><span class="sxs-lookup"><span data-stu-id="1a810-122">Example of an Enumeration</span></span>

<span data-ttu-id="1a810-123">下列程式碼片段說明如何列舉可用的身分識別。</span><span class="sxs-lookup"><span data-stu-id="1a810-123">The following code snippet shows you how to enumerate through available identities.</span></span>


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



