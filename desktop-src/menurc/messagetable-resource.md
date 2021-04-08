---
title: MESSAGETABLE 資源
description: 定義應用程式的訊息資料表資源的識別碼和檔案。 消息表是事件記錄和 FormatMessage 函式中使用的特殊字元串資源。 檔案包含訊息編譯器所產生的二進位訊息資料表，MC.EXE。
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- MESSAGETABLE 資源功能表與其他資源
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36281f7f6415465a6741f461574bca29c681cbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681920"
---
# <a name="messagetable-resource"></a>MESSAGETABLE 資源

定義應用程式的訊息資料表資源的識別碼和檔案。 消息表是事件記錄和 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式中使用的特殊字元串資源。 檔案包含訊息編譯器所產生的二進位訊息資料表，MC.EXE。

訊息編譯器也會產生資源腳本檔案，其中包含在已編譯的資源檔中包含訊息資料表資源所需的 **MESSAGETABLE** 語句。 使用 [**\# include**](-include.md)指示詞將此資源腳本包含在您的主要資源腳本中。

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源的檔案名。 名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例會定義 **MESSAGETABLE** 資源：

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 