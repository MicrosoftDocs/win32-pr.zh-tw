---
title: 顯示功能區
description: Windows 功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區 UI 的方式。
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows 功能區，自訂色彩
- 功能區、自訂色彩
- 自訂 Windows 功能區色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023768"
---
# <a name="displaying-the-ribbon"></a>顯示功能區

Windows 功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區 UI 的方式。

-   [簡介](#introduction)
-   [最小化功能區](#minimize-the-ribbon)
-   [隱藏功能區](#hide-the-ribbon)
-   [範例](#example)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

若要將檔空間的可用區域最大化 (或查看功能區架構應用程式的 [埠]) ，應用程式可以指定功能區 UI 是可見或隱藏，而且在可見時，功能區是否為展開或折迭狀態。

下表所列的 [framework 屬性索引鍵](windowsribbon-reference-properties-framework.md) 可用來明確設定功能區架構應用程式中功能區 UI 的顯示特性。 這些屬性不會影響 [內容快顯功能表](windowsribbon-controls-contextpopup.md) 控制項的顯示。



| 顯示狀態         | 功能區屬性索引鍵                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| 展開或折迭 | [\_ \_ 最小化 UI PKEY](windowsribbon-reference-properties-uipkey-minimized.md) |
| 可見或隱藏     | [UI \_ PKEY \_ 可見](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>最小化功能區

功能區架構應用程式可以將 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性索引鍵的值設定為 **true** 或 **false**，以動態方式設定功能區命令列的最小化狀態。



| 顯示狀態 | 屬性索引鍵值 |
|---------------|--------------------|
| 展開      | **false**          |
| Collapsed     | **true**           |



 

當功能區 UI 處於最小化狀態時，[功能區] 索引標籤資料列會維持可見且功能完整。

下列螢幕擷取畫面顯示最小化狀態的功能區。

![顯示最小化功能區 ui 的螢幕擷取畫面。](images/overviews/ribbon-minimized.png)

> [!Note]  
> 功能區架構會透過功能區內容功能表的 [將功能區最小化] 選項，向終端使用者公開此功能。

 

## <a name="hide-the-ribbon"></a>隱藏功能區

功能區架構應用程式可以將 [UI \_ PKEY 可 \_ 查看](windowsribbon-reference-properties-uipkey-viewable.md) 屬性索引鍵的值設定為 **true** 或 **false**，以動態方式設定功能區命令列的可見狀態。



| 顯示狀態 | 屬性索引鍵值 |
|---------------|--------------------|
| 可見       | **false**          |
| Hidden        | **true**           |



 

相較于 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性，將 [ui PKEY 設定為 \_ \_](windowsribbon-reference-properties-uipkey-viewable.md) **false** ，可將功能區 ui 隱藏，而使用者完全無法使用。

下列螢幕擷取畫面顯示處於隱藏狀態的功能區。

![顯示隱藏功能區 ui 的螢幕擷取畫面。](images/overviews/ribbon-viewable.png)

## <a name="example"></a>範例

下列範例示範如何在執行時間設定功能區 UI 的狀態。

在此情況下， [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 函式是用來根據 [切換按鈕](windowsribbon-controls-togglebutton.md)的切換狀態來展開或折迭功能區 UI。


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[功能區屬性](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 