---
title: 如何使用虛擬 List-View 控制項
description: 本主題將示範如何使用虛擬清單視圖控制項。
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/08/2021
ms.locfileid: "106998968"
---
# <a name="how-to-use-virtual-list-view-controls"></a>如何使用虛擬 List-View 控制項

本主題將示範如何使用虛擬清單視圖控制項。 隨附的 c + + 程式碼範例示範如何處理虛擬清單-view 控制項通知訊息、如何優化快取，以及如何從快取中取得專案。

-   [您必須知道的事項](#what-you-need-to-know)
-   [處理虛擬 List-View 控制通知碼](#process-virtual-list-view-control-notification-codes)
-   [優化快取](#optimize-the-cache)
-   [從快取中取出專案](#retrieve-an-item-from-the-cache)
-   [相關主題](#related-topics)

> [!Note]  
> 本節中的範例程式碼假設快取是應用程式定義結構的動態配置陣列。 結構是在下列 c + + 程式碼範例中定義的。

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="process-virtual-list-view-control-notification-codes"></a>處理虛擬 List-View 控制通知碼

除了其他清單視圖控制項所傳送的通知碼之外，虛擬清單視圖控制項也可以傳送 [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 和 [**LVN \_ ODFINDITEM**](lvn-odfinditem.md) 通知碼。

此應用程式定義的函式會處理通常從虛擬清單-view 控制項傳送的通知訊息。


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a>優化快取

當其顯示區域的內容已變更時，虛擬清單視圖控制項會傳送 [LVN \_ ODCACHEHINT](lvn-odcachehint.md) 通知訊息。 訊息包含要快取之專案範圍的相關資訊。 收到通知訊息時，您的應用程式必須準備好載入具有所要求範圍之專案資訊的快取，如此一來，當傳送 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知訊息時，就可以立即使用該資訊。

在下列 c + + 程式碼範例中，應用程式定義函式會接受虛擬清單-view 控制項所傳送之快取的專案範圍。 它會執行驗證，以判斷所要求的專案範圍尚未快取，然後視需要配置必要的全域記憶體並填滿快取。


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a>從快取中取出專案

這個範例函式會接受兩個參數，也就是應用程式定義結構的位址，以及代表清單中專案索引的整數值。 它會檢查索引值，以探索是否快取所需的專案。 如果是，傳遞至函式的指標會設定為快取中的位置。 如果專案不在主要或結束快取中，則必須以手動方式找出專案資訊。


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a>備註

如需清單視圖控制項所處理的視窗訊息清單，請參閱 [預設 List-View 訊息處理](listview-message-processing.md)。

## <a name="complete-example"></a>完整範例

## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單視圖控制項參考](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 




