---
title: 回應檔命令
description: 回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- 命令列參考 MIDL，回應檔案命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932462"
---
# <a name="the-response-file-command"></a>回應檔命令

回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。 與命令列不同的是，回應檔允許多行的選項和檔案名。 這可能會因為您的組建環境有所限制，或為了方便您建立您的組建流程。

## <a name="switch-options"></a>切換選項

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*回應 \_ 檔*
</dt> <dd>

指定回應檔案的名稱。 回應檔名稱必須緊接在 @ 字元後面。 @ 字元和回應檔名稱之間不允許有空格。

</dd> </dl>

## <a name="remarks"></a>備註

除了在命令列上放置與參數相關聯的所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。 回應檔中的選項會被解讀為 MIDL 命令列中的該位置。

回應檔中的每個引數都必須在同一行的開頭和結尾。 反斜線字元 (\) 不能用來串連行。 當它是回應檔中引號字串的一部分時，反斜線字元只能用在另一個反斜線之前或雙引號字元 ( ") 之前。 當它不是引號字串的一部分時，反斜線字元只能用在雙引號字元之前。

MIDL 支援命令列引數，其中包含一或多個與其他命令列參數結合的回應檔。

MIDL 編譯器不支援嵌套回應檔。

## <a name="examples"></a>範例

**midl @midl.rsp**

**midl-Oicf @midl1.rsp -env win32 @midl2.rsp itf .idl**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




