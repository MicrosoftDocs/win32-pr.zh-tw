---
title: fault_status 屬性
description: '\ 錯誤 \_ 狀態 \ ACF 屬性指定錯誤 \_ 狀態 t 的錯誤碼 \_ 指出遠端程式失敗，而不是其他類型的問題，例如通訊錯誤。'
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status 屬性 MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678251"
---
# <a name="fault_status-attribute"></a>錯誤 \_ 狀態屬性

錯誤 **\[ \_ 狀態 \]** ACF 屬性指定錯誤 [**\_ 狀態 \_ t**](error-status-t.md)的錯誤碼指出遠端程式失敗，而不是其他類型的問題，例如通訊錯誤。

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>參數

<dl> <dt>

*ACF 函式-屬性* 
</dt> <dd>

指定零個或多個 ACF 函數屬性，例如 **\[ 錯誤 \_ 狀態 \]** 和 **\[** [**了 nocode**](nocode.md) **\]** 。 函數屬性以方括弧括住。 請注意，零或多個屬性可以套用至函式。 以逗號分隔多個函式屬性。 另請注意，如果 **\[ 錯誤 \_ 狀態 \]** 顯示為函式屬性，它也不能顯示為參數屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*ACF-參數-屬性* 
</dt> <dd>

指定適用于參數的屬性。 請注意，您可以將零個或更多屬性套用至參數。 參數屬性以方括弧括住。 以逗號分隔多個參數屬性。 ACF 中不允許 IDL 參數屬性（例如方向屬性）。 請注意，如果 **\[ 錯誤 \_ 狀態 \]** 顯示為參數屬性，它也不能顯示為函數屬性。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函數的參數。 函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 錯誤 \_ 狀態 \]** 屬性可以當做函數屬性或參數屬性使用，但每個函數只能出現一次。 它可以套用至函式本身或每個函數中的一個參數。

**\[ 錯誤 \_ 狀態 \]** 屬性只能套用至傳回類型 [**錯誤 \_ 狀態 \_ t**](error-status-t.md)的函式。 當遠端程式失敗，導致傳回錯誤 PDU 時，會傳回錯誤碼。

當 **\[ 錯誤 \_ 狀態 \]** 當做參數屬性使用時，參數必須是 **\[** [](out-idl.md) **\]** [**錯誤 \_ 狀態 \_ t**](error-status-t.md)類型的 out 參數。 如果發生伺服器錯誤，參數會設定為錯誤碼。 當遠端呼叫順利完成時，程式會設定此值。

與 **\[ 錯誤 \_ 狀態 \]** 屬性相關聯的參數，不需要在 IDL 檔案中指定。 如果未指定參數，則會在 DCE IDL 檔案中定義的最後一個參數之後，產生型 [**\_ 別錯誤狀態 \_ t**](error-status-t.md)的新 [**out**](out-idl.md)參數。

**\[ 錯誤 \_ 狀態 \]** 和 **\[** 屬性（attribute） [**\_ 狀態**](comm-status.md) **\]** 屬性（attribute）可能會以函數屬性或參數屬性（attribute）的形式出現在單一函式中。 如果這兩個屬性都是函數屬性，或它們套用至相同參數但未發生任何錯誤，則函數或參數的值 **錯誤 \_ 狀態為 \_ [確定]**。 否則，它會包含適當的狀態碼值。 因為針對 **\[ 錯誤 \_ 狀態 \]** 傳回的值與針對 [ **\[ 通訊 \_ 狀態 \]**] 傳回的值不同，所以會立即解讀傳回的值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**通訊 \_ 狀態**](comm-status.md)
</dt> <dt>

[**錯誤 \_ 狀態 \_ t**](error-status-t.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> </dl>

 

 




