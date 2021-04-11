---
title: 線上列印嚮導
description: Windows Vista Online 列印嚮導可協助使用者訂購相片，使其無法從參與的線上列印零售商進行列印。
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- 線上列印嚮導
- 圖示，線上列印嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315094"
---
# <a name="online-printing-wizard"></a>線上列印嚮導

Windows Vista Online 列印嚮導可協助使用者訂購相片，使其無法從參與的線上列印零售商進行列印。 此 wizard 的設計目的是要讓任何應用程式以程式設計方式叫用它，以便讓使用者能夠訂購相片的列印。 您可以在 Windows Vista 上使用相片列印嚮導。 適用于 Windows 的 PIX

-   [線上列印嚮導所提供的功能](#features-provided-by-the-online-print-wizard)
-   [支援的相片檔案格式](#supported-photo-file-formats)
-   [以程式設計方式啟動線上列印嚮導](#programmatically-launching-the-online-print-wizard)
-   [存取線上列印嚮導圖示](#accessing-the-online-print-wizard-icon)
-   [線上列印嚮導 MRU 屬性](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>線上列印嚮導所提供的功能

Windows Vista Online 列印嚮導可讓使用者從一部參與的線上列印零售商訂購沖印。 叫用時，wizard：

1.  接受要排序列印的檔案或檔案清單。
2.  自動抓取目前參與的線上列印零售商清單，並讓使用者選取要購買相片的零售商。
3.  引導使用者完成進程或訂購列印。

任何應用程式都可以受益于 Windows Vista Online 列印嚮導所提供的功能。 應用程式只需要傳入要排序列印的檔案或檔案，嚮導就會引導使用者完成訂購程式。

下圖顯示 Windows Vista Online 列印嚮導，顯示參與線上列印零售商的範例清單。

![windows vista online 列印嚮導](images/opw.png)

## <a name="supported-photo-file-formats"></a>支援的相片檔案格式

Windows Vista Online 列印嚮導支援已安裝 Windows 影像處理元件 (WIC) 編解碼器的任何影像檔案格式。 WIC 提供數個標準編解碼器，包括：

-   點陣圖 (BMP)
-   圖形交換格式 (GIF)
-    (.ICO) 的圖示格式
-   JPEG 格式 (JPEG)
-   可攜式網路圖形 (PNG)
-   標記的影像檔案格式 (TIFF)
-   Windows Media 相片格式

如需 WIC 和 WIC 編解碼器的詳細資訊，請參閱 [Windows 影像處理元件](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)。

線上列印零售商所支援的檔案格式會因零售商而異;特定零售商可能不支援 Windows Vista Online 列印嚮導所支援的所有檔案格式。 如果使用者嘗試使用所選零售商不支援的格式來訂購列印，則 Windows Vista Online 列印嚮導會通知使用者，選取的零售商不支援所提交的檔案格式。

## <a name="programmatically-launching-the-online-print-wizard"></a>以程式設計方式啟動線上列印嚮導

若要叫用 Windows Vista Online 列印嚮導，請使用下列類別識別碼呼叫 [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面 (CLSID) ：


```
CLSID_PublishDropTarget
```



此 CLSID 定義于 Shobjidl.h .h 和 Shobjidl.h 中。 Windows Vista Online 列印嚮導所要處理的檔案會在 [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) 物件中指定。

下列程式碼範例示範如何叫用 Windows Vista Online 列印嚮導。


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>存取線上列印嚮導圖示

Windows Vista Online 列印嚮導會匯出可由呼叫它的應用程式存取及顯示的圖示。 下圖顯示 Windows Vista Online 列印嚮導圖示。

![windows vista online 列印嚮導圖示](images/opw-icon.png)

下列程式碼範例將示範如何藉由讀取 **OPWIcon** 屬性，來取得 Windows Vista Online 列印嚮導圖示的索引。


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>線上列印嚮導 MRU 屬性

Windows Vista Online 列印嚮導會定義三個與最近使用的 (MRU) 線上列印零售商相關的屬性。



| 屬性名稱 | 屬性值/函數                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | 您可以從這個屬性讀取最近使用之線上列印零售商的圖示索引。                                                                                                                                                                 |
| **MRUName**   | 您可以從這個屬性讀取最近使用的線上列印零售商的名稱。                                                                                                                                                                               |
| **UseMRU**    | **VARIANT** **VT \_ BOOL** 值，表示 wizard 是否應略過線上列印零售商選取頁面，並改用最近使用的線上列印零售商。 將此屬性設定為 **VARIANT \_ TRUE** ，以略過 [零售商選取] 頁面。 |



 

下列程式碼範例示範如何設定 UseMRU 屬性，讓 Windows Vista Online 列印嚮導略過線上列印零售商選取頁面，並自動選取最近使用的零售商。


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



下列程式碼範例示範如何讀取 MRUName 和 MRUIcon 屬性。


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 