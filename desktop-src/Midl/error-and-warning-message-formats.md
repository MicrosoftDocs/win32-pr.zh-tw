---
title: 錯誤和警告訊息格式
description: MIDL 錯誤訊息和警告訊息格式的清單。
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- 錯誤 MIDL，訊息格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384414"
---
# <a name="error-and-warning-message-formats"></a>錯誤和警告訊息格式

命令列錯誤會以下列格式顯示：

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

[其他錯誤資訊] 欄位會根據錯誤訊息提供內容特定的資訊。 例如，當未解決的型別宣告錯誤發生時，[其他錯誤資訊] 欄位會顯示無法解析之類型的名稱。

編譯時期警告會以下列格式顯示：

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

編譯時期錯誤會以下列格式顯示：

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

選擇性內容資訊是指發生錯誤的內容。 當 MIDL 編譯器在類型和程式簽章的語義分析期間發現錯誤時，就會產生此錯誤。 MIDL 編譯器會報告這項資訊，以協助您快速地在 IDL 檔案中找到錯誤。

系統錯誤訊息會以下列格式顯示：

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

此訊息是由非預期的錯誤所產生。 十六進位錯誤號碼是 Windows XP、Windows 2000、Windows NT、Windows 98 或 Windows 95 系統錯誤識別碼。 您可以在 Winerror.h 或 Ntstatus 中找到其他資訊。 如需解決造成此錯誤之狀況的詳細資訊，請參閱 [編譯器錯誤](compiler-errors.md) MIDL9008 的錯誤文字。

 

 




