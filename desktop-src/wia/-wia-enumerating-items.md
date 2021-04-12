---
description: 建立裝置時，Windows 映像取得 (WIA) 會建立 WIA 專案的階層樹狀結構，代表裝置以及與該裝置相關聯的資料夾和影像。
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: 列舉專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192797"
---
# <a name="enumerating-items"></a><span data-ttu-id="3b008-103">列舉專案</span><span class="sxs-lookup"><span data-stu-id="3b008-103">Enumerating Items</span></span>

<span data-ttu-id="3b008-104">建立裝置時，Windows 映像取得 (WIA) 會建立 WIA 專案的階層樹狀結構，代表裝置以及與該裝置相關聯的資料夾和影像。</span><span class="sxs-lookup"><span data-stu-id="3b008-104">When a device is created, Windows Image Acquisition (WIA) creates a hierarchical tree of WIA items that represent the device and the folders and images associated with that device.</span></span> <span data-ttu-id="3b008-105">使用根專案的 (樹狀目錄根目錄中代表裝置的專案) [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (或 [**IWiaItem2：： EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) 方法來建立列舉值物件，並取得其 [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (或 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) 介面的指標，該介面可用來導覽專案樹狀結構並取得影像的存取權，或掃描與裝置相關聯的張床。</span><span class="sxs-lookup"><span data-stu-id="3b008-105">Use the root item's (the item at the root of the tree that represents the device) [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method to create an enumerator object and obtain a pointer to its [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (or [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) interface, which is used to navigate the item tree and gain access to the images or scanning beds associated with the device.</span></span>

<span data-ttu-id="3b008-106">下列範例顯示的函式會以遞迴方式列舉樹狀結構的所有專案，並以傳遞至函式的根專案為開頭。</span><span class="sxs-lookup"><span data-stu-id="3b008-106">The following example shows a function that recursively enumerates all of the items of a tree, beginning with a root item that is passed to the function.</span></span>


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



<span data-ttu-id="3b008-107">此函式會採用參數 **pWiaItem**，其為要列舉之專案樹狀結構之根專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (或 [**IWiaItem2**](-wia-iwiaitem2.md)) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="3b008-107">The function takes the parameter **pWiaItem**, a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (or [**IWiaItem2**](-wia-iwiaitem2.md)) interface of the root item of the item tree to enumerate.</span></span>

<span data-ttu-id="3b008-108">首先，此函式會檢查項目是否為資料夾或是否有附件。</span><span class="sxs-lookup"><span data-stu-id="3b008-108">First, the function checks to see whether the item is a folder or if it has attachments.</span></span> <span data-ttu-id="3b008-109">如果有，則會呼叫 **pWiaItem** 的 [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (或 [**IWiaItem2：：) EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)方法，以建立專案樹狀結構的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="3b008-109">If it does, it then calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method of **pWiaItem** to create an enumerator object for the item tree.</span></span> <span data-ttu-id="3b008-110">如果此呼叫成功，且列舉值有效，則函式會逐一查看子專案，並以遞迴方式在每個專案上呼叫它，將每個專案視為下一個層級子專案的潛在根專案。</span><span class="sxs-lookup"><span data-stu-id="3b008-110">If this call succeeds, and the enumerator is valid, the function iterates through the child items, and recursively calls itself on each item, treating each as a potential root item for the next level of child items.</span></span>

<span data-ttu-id="3b008-111">以這種方式，函式會列舉傳遞給 **EnumerateItems** 之根專案底下的專案樹狀結構的所有分支。</span><span class="sxs-lookup"><span data-stu-id="3b008-111">In this manner, the function enumerates all branches of the item tree below the root item passed to **EnumerateItems**.</span></span>

 

 



