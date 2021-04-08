---
title: IEnumSTATPROPSTG-Compound 檔案的執行
description: IEnumSTATPROPSTG 介面的複合檔案實作為用來列舉屬性（property），這會產生包含統計屬性資料的 STATPROPSTG 結構。
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933513"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>IEnumSTATPROPSTG-Compound 檔案的執行

[**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)介面的複合檔案實作為用來列舉屬性（property），這會產生包含統計屬性資料的 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)結構。 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的執行會管理統計資料，並與目前的複合檔案儲存物件相關聯。

[**IENUMSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) COM 的函式中的函式會建立一個類別，該類別會讀取整個屬性集，並建立可在呼叫 **IEnumSTATPROPSTG：： Clone** 時共用的靜態陣列。

## <a name="when-to-use"></a>使用時機

呼叫 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 的複合檔案執行，以列舉 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，其中包含目前屬性集內屬性的相關資料。 使用屬性儲存介面的複合檔案執行時，請呼叫 [**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 來傳回 **IEnumSTATPROPSTG** 的指標，以管理屬性儲存物件和其中的元素。

## <a name="remarks"></a>備註

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

取得下一個或多個 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構 (*celt* 參數指定的數位) 。 \_如果成功，則傳回 S OK。

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG：： Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

略過 *celt* 中指定的元素數目。 接下來要透過呼叫來列舉的下一個專案，會成為略過專案之後的元素。 \_如果略過 *celt* 元素，則傳回 s OK; \_ 如果略過小於 *celt* 的元素，則傳回 FALSE。

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG：： Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

將資料指標設為列舉的開頭。 如果成功，則傳回 S \_ OK，否則會傳回 Stg. \_ E \_ INVALIDHANDLE。

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

使用 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 的函式來建立陣列的複本。 由於構成靜態陣列的類別實際上包含物件，因此這個函式主要會加入至參考計數。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 