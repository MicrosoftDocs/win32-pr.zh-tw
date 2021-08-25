---
title: 超屬性
description: 關鍵字 [超] 表示可以宣告為帶正負號或不帶正負號的64位整數。
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- 超屬性 MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f202890d2d81dcd7916f29c0330bf8e7093a7cf189e7b76a8af64dd2f0d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895258"
---
# <a name="hyper-attribute"></a>超屬性

關鍵字 [ **超** ] 表示可以宣告為帶正負號或不帶正負號的64位整數。

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>參數

<dl> <dt>

*宣告子清單* 
</dt> <dd>

指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。 未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

**超** 類型是介面定義語言 (IDL) 的其中一種基底類型。 **超** 型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

> [!Note]  
> 若是16位平臺，MIDL 編譯器會以 **midl \_ uhyper** 取代不帶正負號的超整數。 這允許在不直接支援64位整數的平臺上，定義不帶正負號之超整數的介面。 **MIDL \_ uhyper** 是在 RPC 標頭檔中定義。

 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




