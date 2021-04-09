---
title: 'PROPSETFLAG 常數 (Propidl.idl) '
description: 定義屬性集的特性。
ms.assetid: 6f865c8f-bbca-4122-b076-14f2bc56f292
topic_type:
- apiref
api_name:
- PROPSETFLAG_DEFAULT
- PROPSETFLAG_NONSIMPLE
- PROPSETFLAG_ANSI
- PROPSETFLAG_UNBUFFERED
- PROPSETFLAG_CASE_SENSITIVE
api_location:
- Propidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8f31d7b2659eeaa003c1a0d15103e94ad1a5c89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934428"
---
# <a name="propsetflag-constants"></a>PROPSETFLAG 常數

PROPSETFLAG 常數會定義屬性集的特性。 下表所列的值用於 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)方法、 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)函式和 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)函數的 *grfFlags* 參數中。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROPSETFLAG_DEFAULT"></span><span id="propsetflag_default"></span><dl> <dt>**PROPSETFLAG \_預設值**</dt> <dt>0</dt> </dl>                       | 如果未指定，根據預設，只有簡單的屬性值可以寫入屬性集。 使用簡單的屬性值可防止在複合檔案和獨立的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)執行中交易屬性集。 非 e 屬性值必須用於此用途。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PROPSETFLAG_NONSIMPLE"></span><span id="propsetflag_nonsimple"></span><dl> <dt>**PROPSETFLAG \_簡單**</dt> <dt>1</dt> </dl>                 | 如果有指定，就可以將簡單屬性值寫入屬性集，並將屬性集儲存在儲存物件中。 非簡單的屬性值包括具有 VT 儲存的 VARTYPE \_ 、vt \_ 資料流程、vt \_ 儲存 \_ 物件或 vt \_ 資料流程 \_ 物件的值。 如果未指定此旗標，則無法將非簡單類型寫入屬性集。 在複合檔案和獨立的執行中，只有在指定 **PROPSETFLAG \_ 簡單** 時，才可以交易屬性集。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="PROPSETFLAG_ANSI"></span><span id="propsetflag_ansi"></span><dl> <dt>**PROPSETFLAG \_ANSI**</dt> <dt>2</dt> </dl>                                | 如果有指定，屬性集中所有非明確 Unicode 的字串值（也就是 VT LPWSTR 以外的字串值） \_ 都會與目前的系統 ANSI 字碼頁一併儲存。 如需詳細資訊，請參閱 [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp)。 不建議使用此值。 如需詳細資訊，請參閱＜備註＞。<br/> 如果此值不存在，新屬性集中的字串值會儲存為 Unicode。 此值所提供的控制程度是必要的，如此一來，使用屬性相關介面的用戶端就可以與標準屬性集交互操作，例如 OLE2 摘要資訊（可能存在於 ANSI 字碼頁中）。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PROPSETFLAG_UNBUFFERED"></span><span id="propsetflag_unbuffered"></span><dl> <dt>**PROPSETFLAG \_未緩衝**</dt> <dt>4</dt> </dl>              | 只能搭配 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 和 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) 函數使用;亦即，在屬性集介面的獨立執行中。 如果在這些函式中指定，則不會緩衝處理屬性集的變更。 相反地，變更一律會直接寫入屬性集。 對屬性集 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 方法的呼叫將會變更它。 不過，根據預設，變更會在內部屬性集快取中進行緩衝處理，然後在呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 方法時，寫入屬性集。 <br/> 設定 **PROPSETFLAG 無 \_ 緩衝** 會降低效能，因為在每次變更屬性集之後，會自動清除屬性集內部緩衝區。 不過，直接寫入變更可防止協調問題。 例如，如果在交易模式中開啟儲存物件，則會緩衝處理屬性集。 然後，如果您在儲存物件上呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 方法，則不會將屬性集變更視為交易的一部分，因為它們位於尚未排清的緩衝區中。 您必須在呼叫 **IStorage：： commit** 之前呼叫 [**IPropertyStorage：： commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ，以排清屬性集緩衝區，然後再認可對儲存體的變更。 除了進行兩個呼叫之外，您還可以設定 **PROPSETFLAG 無 \_ 緩衝** ，讓變更一律直接寫入屬性集，且永遠不會在屬性集的內部快取中進行緩衝處理。 然後，在認可交易儲存體時，就會挑選變更。<br/> |
| <span id="PROPSETFLAG_CASE_SENSITIVE"></span><span id="propsetflag_case_sensitive"></span><dl> <dt>**PROPSETFLAG \_區分 \_ 大小寫**</dt> <dt>8</dt> </dl> | 如果有指定，屬性名稱會區分大小寫。 只有在第1版的屬性集序列化格式中，才可以區分大小寫的屬性名稱。 如需詳細資訊，請參閱 [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>備註

您可以使用位運算來設定和檢查這些值，以決定如何建立和開啟屬性集。 屬性集是使用 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 方法或 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 函數所建立。 它們是使用 [**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 方法或 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) 函數來開啟。

建議您不要在 *grfFlags* 參數中設定 **PROPSETFLAG \_ ANSI** 旗標，以將屬性集建立為 Unicode。 此外，也建議您避免使用 VT \_ LPSTR 值，並改為使用 vt \_ LPWSTR 值。 當屬性集字碼頁是 Unicode 時，VT \_ LPSTR 字串值會在儲存時轉換成 unicode，並在抓取時轉換回多位元組字元串值。 當屬性集的字碼頁不是 Unicode 時，屬性名稱、VT \_ BSTR 字串和簡單屬性值會在儲存時轉換成多位元組字元串，並且在抓取時轉換回 Unicode，全都使用目前的系統 ANSI 字碼頁。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Propidl.idl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FmtIdToPropStgName**](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
</dt> <dt>

[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dt>

[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dt>

[**PropStgNameToFmtId**](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> </dl>

 

