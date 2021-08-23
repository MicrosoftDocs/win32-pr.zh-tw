---
title: 字型語句
description: 定義系統在對話方塊中用來繪製文字的字型。 字型必須先前已載入;例如，藉由呼叫 LoadResource 函數。
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- 字型語句功能表和其他資源
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972067"
---
# <a name="font-statement"></a>字型語句

定義系統在對話方塊中用來繪製文字的字型。 字型必須先前已載入;例如，藉由呼叫 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 函數。

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*dialog*
</dt> <dd>

字型的大小（以點為單位）。

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*字體*
</dt> <dd>

字樣的名稱。 此參數必須以引號括住 ( ") 。

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*重量*
</dt> <dd>

範圍0到1000的字型粗細。 例如，400是正常的，700是粗體。 如果這個值為0，則會使用預設權數。 如需預先定義的值清單，請參閱 WinGDI 中定義的 **FW \_ \*** 值。

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*斜*
</dt> <dd>

如果設定為 TRUE，則表示斜體字型。

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*字元集*
</dt> <dd>

字元集。 如需值的清單，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfCharSet** 成員。

</dd> </dl>

## <a name="examples"></a>範例

下列範例示範 **字型** 語句的用法：

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 