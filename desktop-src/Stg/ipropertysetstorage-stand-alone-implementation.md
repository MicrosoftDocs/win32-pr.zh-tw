---
title: IPropertySetStorage-獨立執行
description: 系統提供的 IPropertySetStorage 獨立執行包括 IPropertyStorage 和 IPropertySetStorage 的實作為。
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd Stg.，實施
- IPropertySetStorage Strctd Stg.，獨立部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b4aec27afd0e02ffcb9886f13de2a17761c66eab106665fe4143ab42c86a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961277"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage-獨立執行

系統提供的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 獨立執行包括 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 **IPropertySetStorage** 的實作為。[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 是在屬性集儲存體中讀取和寫入屬性的介面。 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 是在儲存體中建立和開啟屬性集的介面。 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)和 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面也會在獨立的執行中提供。

若要使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的獨立執行，請先取得系統提供的獨立執行的指標，並將系統提供的實作為您的儲存物件。 若要取得 **IPropertySetStorage** 之獨立執行的指標，請呼叫 [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) 函數，並提供 *pStorage* 參數，以指定將包含屬性集的儲存物件。 這個函式會為指定的儲存物件提供新 **IPropertySetStorage** 介面的指標。

獨立的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 執行會在任何儲存物件上建立屬性集，而不只是在複合檔案儲存體上建立。 獨立的執行不相依于複合檔案，並且可搭配任何結構化儲存體的執行使用。 呼叫端提供的結構化儲存體有任何限制適用于這個屬性集的執行。 例如，如果您提供簡單模式的儲存體給 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)，所產生的 **IPropertySetStorage** 將會受到所提供 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的限制。

如需此介面之複合檔案執行的詳細資訊，請參閱 [IPropertySetStorage-複合檔案執行](ipropertysetstorage-compound-file-implementation.md)一節。

## <a name="when-to-use"></a>使用時機

呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的方法，以建立、開啟及刪除任何結構化儲存體中的屬性集。 另外還有一種方法，它會提供指向 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 列舉值的指標，可用來列舉儲存區中的屬性集。

獨立的執行也會提供 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 和 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper 函式（除了 [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 和 [**open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 方法），以建立和開啟屬性集。 這兩個函式會新增 PROPSETFLAG \_ 無緩衝值的支援，讓您可以直接將變更寫入屬性集，而不是在快取中緩衝處理。 如需詳細資訊，請參閱 [**PROPSETFLAG 常數**](propsetflag-constants.md)。

## <a name="methods"></a>方法

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的獨立執行支援下列方法。

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

在儲存體中建立新的屬性集，並將指標傳回屬性集上的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。

如果您打算使用 PROPSETFLAG \_ 無緩衝的值，請改用 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 函式來建立並開啟新的屬性集，並在屬性集上取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面之獨立執行的指標。

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

在儲存體中開啟現有的屬性集，並將指標傳回屬性集上的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。

如果您打算使用 PROPSETFLAG \_ 無緩衝的值，請改用 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) 函式來取得指定之屬性集上 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 獨立執行的指標。

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage：:D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

刪除這個屬性集儲存體中設定的屬性。

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

建立可用於列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的物件。 每個 **STATPROPSETSTG** 結構都會提供單一屬性集的相關資料。

> [!Note]  
> DocumentSummaryInformation 和使用者設定的屬性集是唯一的，因為它在單一基礎資料流程中可能有兩個屬性集區段。 如需詳細資訊，請參閱 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md) 。

 

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPropertyStorage-獨立執行](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage：： EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**PROPSETFLAG 常數**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**STGM 常數**](stgm-constants.md)
</dt> </dl>

 

 