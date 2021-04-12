---
description: 描述如何使用集合介面的一般方法。
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: 使用 XPS OM 集合介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193374"
---
# <a name="working-with-xps-om-collection-interfaces"></a>使用 XPS OM 集合介面

描述如何使用集合介面的一般方法。

## <a name="contents"></a>目錄

本節所述的方法會顯示在下列清單中。 並非所有的集合介面都支援這些方法，而某些介面也支援此頁面上未描述的方法。 如需特定介面所支援的方法清單，請參閱該介面描述的描述。

<dl>

[Append 方法](#append-method)  
[GetAt 方法](#getat-method)  
[GetCount 方法](#getcount-method)  
[InsertAt 方法](#insertat-method)  
[RemoveAt 方法](#removeat-method)  
[SetAt 方法](#setat-method)  
</dl>

[另請參閱](#see-also)

## <a name="append-method"></a>Append 方法

將物件附加至集合的結尾。

**泛型語法**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**說明**

在集合的結尾，這個方法會附加在參數清單中傳遞的物件，如下圖所示。

![顯示附加專案如何將專案加入至集合的圖表](images/generic-append.png)

## <a name="getat-method"></a>GetAt 方法

從集合中的指定位置取得物件。

**泛型語法**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**說明**

將儲存在集合 *位置的物件，寫入至**物件* 所參考的變數。 這個動作不會變更集合的內容。 下圖說明此程序。

![顯示 getat 如何從集合中抓取專案的圖表](images/generic-getat.png)

## <a name="getcount-method"></a>GetCount 方法

取得儲存在集合中的物件數目。

**泛型語法**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**說明**

將目前儲存在集合中的物件數目寫入至 *count* 所參考的變數中。 這個動作不會變更集合的內容。 下圖說明此程序。

![此圖顯示 getcount 如何取得集合中的專案數](images/generic-getcount.png)

## <a name="insertat-method"></a>InsertAt 方法

將物件插入集合中指定的位置。

**泛型語法**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**說明**

在 *物件* 中傳遞的物件會插入至集合中 *索引* 所指定的位置。 在插入新的 *物件* 之前，此方法會將先前已佔用位置的物件移至 1 *，並移動**索引* 後面的所有介面指標。 下圖說明此程序。

![顯示 insertat 如何將專案加入至集合的圖表](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt 方法

從集合中的指定位置移除物件。

**泛型語法**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**說明**

這個方法會從 *索引* 所指定的位置釋出物件，然後藉由減少 *索引* 後面每個指標的索引，來壓縮集合。 下圖說明此程序。

![顯示 removeat 如何從集合中移除專案的圖表](images/generic-removeat.png)

## <a name="setat-method"></a>SetAt 方法

取代集合中位於指定位置的物件。

**泛型語法**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**說明**

這個方法會先在 *索引* 所參考的位置釋出物件，然後以 *物件* 中所傳遞的物件來取代該物件。 下圖說明此程序。

![此圖顯示 setat 如何取代集合中的專案](images/generic-setat.png)

## <a name="see-also"></a>另請參閱

<dl>

[**IXpsOMColorProfileResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**IXpsOMGradientStopCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**IXpsOMSignatureBlockResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



