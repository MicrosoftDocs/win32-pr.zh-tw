---
title: IEnumSTATPROPSETSTG-Compound 檔案的執行
description: IEnumSTATPROPSETSTG 介面的複合檔案實作為列舉包含統計屬性資料之 STATPROPSETSTG 結構的陣列。
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315334"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>IEnumSTATPROPSETSTG-Compound 檔案的執行

[**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面的複合檔案實作為列舉包含統計屬性資料之 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)結構的陣列。 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)執行會管理統計資料，並與目前的複合檔案儲存物件相關聯。

## <a name="when-to-use"></a>使用時機

呼叫 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 的方法來列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構，其中每一個都提供與複合檔案儲存物件相關聯的其中一個屬性集的相關資料。

## <a name="remarks"></a>備註

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

取得下一個或多個 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構 (*celt* 參數指定的數位) 。 透過呼叫 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的複合檔案執行所提供的 **STATPROPSETSTG** 元素，請遵循下列規則：

-   如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 無法提供 STATPROPSETSTG. fmtid，則會將零寫入至該成員。 當屬性集沒有預先定義的名稱 (（例如 \\ 005SummaryInformation) ，而且不是合法值）時，就會發生這種情況。
-   DocumentSummaryInformation 和使用者設定的屬性集是特殊的，因為它可能有兩個屬性集區段。 這個屬性集的說明位於 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)一節中。 第二個區段稱為 User-Defined 屬性。 每個區段都會以唯一的格式識別碼來識別 (FMTID) 。 當使用 [**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) 來列舉屬性集時，將不會列舉 User-Defined 的屬性集。

> [!Note]  
> 如果您一律使用 [**IPropertySetStorage：： create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)來建立屬性集，則因為系統會為儲存體名稱建立「字元 GUID」，所以 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 會傳回非零的有效 FMTID （property set \[ STATPROPSETSTG. FMTID） \] 。

 

-   STATPROPSETSTG. grfFlags 成員不一定會反映屬性集是否為 ANSI。 如果 \_ 已設定 PROPSETFLAG ANSI，則屬性集絕對是 ANSI。 如果 PROPSETFLAG \_ ANSI 很清楚，屬性集可以是 unicode 或非 unicode，因為無法判斷它是否為 ANSI 而不需要開啟。
-   STATPROPSETSTG. grfFlags 成員會反映屬性集是否為簡單的，因此 PROPSETFLAG 簡單旗標的設定 \_ 一律有效。
-   如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 無法提供 STATPROPSETSTG，則會將它設定為所有零 (clsid \_ Null) 。 在 COM 複合檔案執行中，當屬性集很簡單 (PROPSETFLAG 簡單旗標未 \_ 設定) 或簡單，但未明確設定 CLSID 時，就會發生這種情況。 針對簡單屬性集，所接收的 CLSID 是基礎 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)所維護的 CLSID。
-   如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)無法提供 \[ **ctime**、 **mtime**、 **atime** 的時間欄位 \] ，則每個不支援的時間將會設定為零。 在 COM 複合檔案執行中，取得這些值取決於從基礎 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 執行中取得這些值。

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG：： Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

略過 *celt* 中指定的元素數目。 \_如果略過指定的元素數目，則傳回 s OK， \_ 如果略過要求的元素數目較少，則傳回 FALSE。 在其他任何情況下，都會傳回適當的錯誤。

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG：： Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

將資料指標設為列舉的開頭。 如果成功，則傳回 S \_ OK，否則會傳回 Stg. \_ E \_ INVALIDHANDLE。

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

複製這個列舉值的目前列舉狀態。

</dd> </dl>

 

 