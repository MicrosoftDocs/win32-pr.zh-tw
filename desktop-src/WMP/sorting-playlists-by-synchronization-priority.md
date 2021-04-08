---
title: 依同步處理優先順序排序播放清單
description: 依同步處理優先順序排序播放清單
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Windows Media Player，同步播放清單
- Windows Media Player 物件模型，同步播放清單
- 物件模型，同步處理播放清單
- Windows Media Player 行動裝置、同步播放清單
- Windows Media Player ActiveX 控制項，同步播放清單
- Windows Media Player 的行動 ActiveX 控制項、同步播放清單
- ActiveX 控制項，同步播放清單
- 播放清單，同步處理
- 中繼檔播放清單，同步處理
- Windows Media 中繼檔播放清單，同步處理
- 可攜式裝置，排序同步播放清單
- 同步播放清單，排序
- 同步播放清單，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841904"
---
# <a name="sorting-playlists-by-synchronization-priority"></a>依同步處理優先順序排序播放清單

下列程式碼會執行簡單排序的播放清單。 您可以在 [列舉同步播放清單](enumerating-synchronization-playlists.md)的範例程式碼中，看到此函式的使用方式。 函數會採用下列參數：

-   *pPlaylist*。 要排序之 Windows Media Player 播放清單的指標。 播放清單中的媒體專案必須指向其他播放清單，而不是個別的數位媒體檔案。
-   *bstrSyncAttribute*。 包含目前裝置之同步合作關係屬性名稱的 BSTR ( "Sync01"、"Sync02" 等等) 。
-   *plSelected*。 **長** 變數的指標，此變數會接收同步播放清單的計數。

此函式會檢查每個媒體專案的同步合作關係屬性 (代表 *pPlaylist* 所指定播放清單中的播放清單) 。 如果屬性具有非零值，則程式碼會將媒體專案移至播放清單的開頭，並依優先權順序插入。

完成時，此函式會傳回 (同步處理的播放清單) 之媒體專案的計數，這是同步合作關係屬性的非零值。


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPMedia：： getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPPlaylist：： get \_ 專案**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**IWMPPlaylist：： moveItem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**管理同步播放清單**](managing-synchronization-playlists.md)
</dt> <dt>

[**同步屬性**](sync-attributes.md)
</dt> </dl>

 

 




