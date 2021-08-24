---
description: 建立裝置時，Windows 映像取得 (wia) 會建立 WIA 專案的階層樹狀結構，以代表裝置以及與該裝置相關聯的資料夾和影像。
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: 列舉專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438e5cb65b701fcbc24d61aa888ac6c88347cacdaca8fa0a861f8c452a1ebc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772878"
---
# <a name="enumerating-items"></a>列舉專案

建立裝置時，Windows 映像取得 (wia) 會建立 WIA 專案的階層樹狀結構，以代表裝置以及與該裝置相關聯的資料夾和影像。 使用根專案的 (樹狀目錄根目錄中代表裝置的專案) [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (或 [**IWiaItem2：： EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) 方法來建立列舉值物件，並取得其 [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (或 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) 介面的指標，該介面可用來導覽專案樹狀結構並取得影像的存取權，或掃描與裝置相關聯的張床。

下列範例顯示的函式會以遞迴方式列舉樹狀結構的所有專案，並以傳遞至函式的根專案為開頭。


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



此函式會採用參數 **pWiaItem**，其為要列舉之專案樹狀結構之根專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (或 [**IWiaItem2**](-wia-iwiaitem2.md)) 介面指標。

首先，此函式會檢查項目是否為資料夾或是否有附件。 如果有，則會呼叫 **pWiaItem** 的 [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (或 [**IWiaItem2：：) EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)方法，以建立專案樹狀結構的枚舉器物件。 如果此呼叫成功，且列舉值有效，則函式會逐一查看子專案，並以遞迴方式在每個專案上呼叫它，將每個專案視為下一個層級子專案的潛在根專案。

以這種方式，函式會列舉傳遞給 **EnumerateItems** 之根專案底下的專案樹狀結構的所有分支。

 

 



