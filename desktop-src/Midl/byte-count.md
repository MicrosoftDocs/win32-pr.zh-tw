---
title: byte_count 屬性
description: '\ Byte \_ count \ ACF 屬性是一個參數屬性，可將大小（以位元組為單位）與指標所指示的記憶體區域產生關聯。'
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count 屬性 MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312849"
---
# <a name="byte_count-attribute"></a>byte \_ count 屬性

**\[ Byte \_ count \]** ACF 屬性是一個參數屬性，可將大小（以位元組為單位）與指標所指示的記憶體區域產生關聯。

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*函數-屬性清單* 
</dt> <dd>

指定零個或多個 ACF 函數屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函數的名稱。 需要函數名稱。

</dd> <dt>

*長度-變數名稱* 
</dt> <dd>

指定 *參數* 名稱所參考的記憶體區域大小 [**（以位元組 \[ \]**](in.md)為單位），指定僅限指定的參數名稱。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中所定義之 [**\[ out \]**](out-idl.md)指標參數的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

ACF 屬性 **\[ 位元組 \_ 計數 \]** 表示 MICROSOFT 的延伸至 DCE IDL 的延伸模組。 因此，當您使用 MIDL 編譯器參數 [**/osf**](-osf.md)時，就無法使用這個屬性。

> [!Note]  
> 因為估計所有 [**\[ out \]**](out-idl.md)參數所需的大小，所以 NDR64 語法不再支援 **\[ byte count \]** 屬性。

 

指標參數所參考的記憶體是連續的，而且不會由用戶端存根配置或釋放。 [ **\[ 位元組 \_ 計數 \]** ] 屬性的這項功能可讓您在用戶端記憶體中建立持續性緩衝區區域，以便在多個遠端程序呼叫期間重複使用。

關閉用戶端 stub 記憶體配置的能力可讓您調整應用程式的效率。 例如，使用 Microsoft RPC 的服務提供者函數可使用 **\[ byte \_ count \]** 屬性。 當使用者應用程式呼叫服務提供者 API 並將指標傳送至緩衝區時，服務提供者可以將緩衝區指標傳遞至遠端函式。 服務提供者可以在多個遠端呼叫期間重複使用緩衝區，而不會強制使用者重新配置記憶體區域。

記憶體區域可以包含包含多個指標的複雜資料結構。 因為記憶體區域是連續的，所以應用程式不需要進行數個呼叫來個別釋放每個指標和結構。 相反地，它可以透過呼叫記憶體配置或免費常式來配置或釋放記憶體區域。

緩衝區必須是 [**\[ \] out**](out-idl.md)參數，而緩衝區長度（以位元組為單位） [**\[ \] 必須是僅供使用的**](in.md)參數。

指定夠大的緩衝區，以包含所有 [**\[ out \]**](out-idl.md)參數。 由於隱藏填補的原因，請使用 overestimates，而不是確切的計數。 例如，4位元組指標會在32位平臺上以4位元組對齊的界限，以及64位平臺上8位元組界限上的8位元組指標取消封送。 因此，必須在緩衝區的空間中考慮存根要執行的對齊填補。 此外，C 語言編譯期間使用的封裝層級可能會有所不同。 使用 [位元組計數] 值，以針對 C 語言編譯期間所使用的封裝層級新增額外的封裝位元組。 涵蓋32位平臺和64位平臺的安全做法，是假設每個進入海量儲存體區塊的物件都是從屬於8的倍數的位址開始。

## <a name="examples"></a>範例

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> </dl>

 

 




