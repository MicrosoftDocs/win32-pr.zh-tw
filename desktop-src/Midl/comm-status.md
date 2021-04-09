---
title: comm_status 屬性
description: '\_當函式執行期間發生通訊錯誤時，\ 通訊狀態 \ ACF 屬性會導致傳回錯誤碼。'
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status 屬性 MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678719"
---
# <a name="comm_status-attribute"></a>comm \_ status 屬性

當函數執行期間發生通訊錯誤時，[ **\[ 通訊 \_ 狀態 \]** ACF] 屬性會導致傳回錯誤碼。

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*ACF 函式-屬性* 
</dt> <dd>

指定零個或多個 ACF 函數屬性，例如， **\[ comm \_ status \]** 和 **\[** [**了 nocode**](nocode.md) **\]** 。 函數屬性以方括弧括住。 有零或多個屬性可以套用至函數。 以逗號分隔多個函式屬性。 請注意，如果 **\[ 通訊 \_ 狀態 \]** 顯示為函式屬性，它也不能顯示為參數屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*ACF-參數-屬性* 
</dt> <dd>

指定適用于參數的屬性。 請注意，您可以將零個、一個或多個屬性套用至參數。 以逗號分隔多個參數屬性。 參數屬性以方括弧括住。 ACF 中不允許 IDL 參數屬性（例如方向屬性）。 請注意，如果 **\[ 通訊 \_ 狀態 \]** 顯示為參數屬性，它也不能顯示為函式屬性。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函數的參數。 函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用 [ **\[ comm \_ status \]** ] 屬性做為函數屬性或參數屬性，但每個函式只能出現一次。 它可以套用至函式或每個函式中的一個參數。

[ **\[ Comm \_ status \]** ] 屬性只能套用至傳回型 [**\_ 別錯誤狀態 \_ t**](error-status-t.md)的函式。 在函數執行期間發生通訊錯誤時，會傳回錯誤碼。

當使用訊息 **\[ \_ \] 狀態** 做為參數屬性時，參數必須在 IDL 檔案中定義，而且必須是 **\[** [](out-idl.md) **\]** 類型 [**錯誤 \_ 狀態 \_ t**](error-status-t.md)的 out 參數。 當函數執行期間發生通訊錯誤時，參數會設定為錯誤碼。 當遠端呼叫順利完成時，程式會設定此值。

**\[ 通訊 \_ 狀態 \]** 和 **\[** [**錯誤 \_ 狀態**](fault-status.md) **\]** 屬性可能會以函數屬性或參數屬性的形式出現在單一函式中。 如果這兩個屬性都是函數屬性，或它們套用至相同參數但未發生任何錯誤，則函數或參數的值 **錯誤 \_ 狀態為 \_ [確定]**。 否則，它會包含適當的 **\[ 通訊 \_ 狀態 \]** 或 **\[ 錯誤 \_ 狀態值 \]** 。 由於針對 [狀態] **\[ \_ 狀態 \]** 傳回的值與 **\[ 錯誤 \_ \] 狀態** 傳回的值不同，因此會立即解讀傳回的值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**錯誤 \_ 狀態 \_ t**](error-status-t.md)
</dt> <dt>

[**錯誤 \_ 狀態**](fault-status.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> </dl>

 

 




