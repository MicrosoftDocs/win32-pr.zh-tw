---
description: 說明如何從檔案將現有的 XPS 檔讀取至 XPS OM。
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: 將 XPS 檔讀入 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320264"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>將 XPS 檔讀入 XPS OM

說明如何從檔案將現有的 XPS 檔讀取至 XPS OM。

若要從 XPS 檔建立 XPS OM，請呼叫 [**IXpsOMObjectFactory：： CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) 方法。

在您的程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

## <a name="code-example"></a>程式碼範例

下列程式碼範例假設 [初始化 XPS OM](xps-object-model-initialization.md) 中所述的初始化成功。


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



若要從儲存為數據流的 XPS 檔建立 XPS OM，請呼叫 [**IXpsOMObjectFactory：： CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream)。

## <a name="remarks"></a>備註

如果您在讀取 XPS 封裝之後立即撰寫 XPS OM，部分原始內容可能會遺失或變更。

這種情況下可能會發生的一些變更，如下表所示：

| 檔功能                      | 動作                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| 數位簽章<br/>         | 從檔中移除<br/>                               |
| DiscardControl 元件<br/>        | 從檔中移除<br/>                               |
| 外部檔部分<br/>     | 從檔中移除<br/>                               |
| FixedPage 標記<br/>           | 從原始的修改<br/>                              |
| 資源字典標記<br/> | 如果已設定優化旗標，則從原始修改<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[流覽 XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[將文字寫入至 XPS OM](write-text-to-an-xps-om.md)
</dt> <dt>

[在 XPS OM 中繪製圖形](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[以 XPS OM 放置影像](place-images-in-an-xps-om.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[封裝 API](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

