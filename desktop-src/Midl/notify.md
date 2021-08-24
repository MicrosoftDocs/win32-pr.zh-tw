---
title: 通知屬性
description: '\ Notify \ 屬性會指示 MIDL 編譯器在應用程式的伺服器端產生對 \ notify \ 程式的呼叫。'
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- 通知屬性 MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf1bb1c4f522cecb5fe81a317267e2cffff2da638e3a8c09a412ae8d94a149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066858"
---
# <a name="notify-attribute"></a>通知屬性

[ **\[ 通知 \]** ] 屬性會指示 MIDL 編譯器在應用程式的伺服器端產生 **\[ 通知 \]** 程式的呼叫。

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>參數

<dl> <dt>

*程式-名稱* 
</dt> <dd>

將與通知程式相關聯的遠端程式名稱。

</dd> </dl>

## <a name="remarks"></a>備註

[ **\[ 通知 \]** ] 屬性所呼叫的 **\[ 通知 \]** 程式，會與伺服器上的特定遠端程式相關聯。 它類似于回呼函數的概念。 Stub 會在其相關聯的遠端程式的所有輸出引數都經過封送處理，並釋放與參數相關聯的任何記憶體之後，呼叫 **\[ 通知 \]** 程式。 如果呼叫在伺服器常式執行之前失敗，則會呼叫 **\[ 通知 \]** 常式。 例如，如果伺服器因為從用戶端收到不正確的資料而在封送時失敗， \[ 則 \] 會呼叫通知常式。

在遠端程式中開發取得資源的應用程式時，[ **\[ 通知 \]** ] 屬性會很有用。 然後，這些資源就會在遠端程式的輸出參數完全封送處理之後，于 **\[ 通知 \]** 程式中釋出。

**\[ 通知 \]** 程式名稱是以 [ **\_ 通知**] 尾碼的遠端程式名稱。 **\_ 通知** 程式不需要任何參數，也不會傳回結果。 這項程式的原型也會在標頭檔中產生。 例如，如果 IDL 檔案包含下列內容：

``` syntax
MyProcedure([in] short S);
```

在 ACF for MIDL 中指定下列各項，以產生 **\_ 通知** 呼叫：

``` syntax
[notify] MyProcedure();
```

MIDL 編譯器將會產生包含下列 **\_ 通知** 程式呼叫的伺服器 stub 程式碼：

``` syntax
MyProcedure_notify();
```

標頭檔將包含原型：

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>範例

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> </dl>

 

 




