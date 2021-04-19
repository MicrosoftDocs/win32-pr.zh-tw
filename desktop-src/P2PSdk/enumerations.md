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
# <a name="enumerations-peer-infrastructure"></a> (對等基礎結構) 的列舉

藉由使用列舉，您可以取得符合準則的所有特定對等實體清單。

**取得列舉並取得結果**

1.  取得列舉的控制碼。 呼叫 **PeerEnum** 函式，例如，呼叫 [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) 對等圖形函數。 **PeerEnum** 函式會建立列舉，並將該列舉的控制碼傳回給呼叫應用程式。 您必須使用這個控制碼來取得結果。
2.  （選擇性）取得列舉中的實體數目。 呼叫 **GetItemCount** 函數，例如，呼叫 [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) 或 [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)。
    > [!Note]  
    > 您可以使用 **GetItemCount** 函式所傳回的值來判斷可供取出的專案數目。

     

3.  取出結果群組。 呼叫 **GetNextItem** 函數，例如，呼叫 [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)。
    > [!Note]  
    > 當應用程式呼叫 **GetNextItem** 函式時，它會指定要傳回的實體數目，然後函式會傳回實體指標陣列的指標，以及實體數目（永遠小於或等於指定的數目）。 應用程式可能需要多次呼叫此函數，直到傳回的實體數目小於要求的數目。

     

4.  不需要資料之後，請釋放資料的指標。 呼叫 **FreeData** 函數，例如，呼叫 [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) 或 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)。
    > [!Note]  
    > 如需詳細資訊，請參閱 [釋放對等資料](freeing-peer-data.md)。

     

5.  應用程式不需要列舉的控制碼之後，請加以釋放。 呼叫 **EndEnumeration** 函數，例如，呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) 或 [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)。

## <a name="example-of-an-enumeration"></a>列舉的範例

下列程式碼片段說明如何列舉可用的身分識別。


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



 

 



