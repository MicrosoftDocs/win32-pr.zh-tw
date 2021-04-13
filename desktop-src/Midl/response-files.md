---
title: 回應檔
description: 除了在命令列上放置所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL 編譯器 MIDL，回應檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/07/2019
ms.locfileid: "104372714"
---
# <a name="response-files"></a>回應檔

除了在命令列上放置所有選項以外，MIDL 編譯器還接受包含參數和引數的回應檔。 回應檔是一個文字檔，其中包含一個或多個 MIDL 編譯器命令列選項。 與命令列不同的是，回應檔允許多行的選項和檔案名。 這可能會因為您的組建環境有所限制，或為了方便您建立您的組建流程。 您可以指定 MIDL 回應檔，如下所示：

**midl** **\@ 檔案名**

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

指定回應檔的名稱。 回應檔名稱必須緊接在 @ 字元之後，@ 字元和回應檔名稱之間不能有空白字元。

</dd> </dl>

回應檔中的選項會被解釋為在 MIDL 命令列中出現的位置。 回應檔中的每個引數都必須在同一行的開頭和結尾。 您無法使用反斜線字元 (\) 來串連行。

MIDL 支援包含一或多個回應檔的命令列引數，並與其他命令列參數結合：

**midl-Oicf @midl1.rsp -envwin32 @midl2.rsp itf .idl**

MIDL 編譯器不支援嵌套回應檔。

 

 




