---
title: Type_UserFree 函式
description: 型 \_ 別 UserFree 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682393"
---
# <a name="the-type_userfree-function"></a>型別 \_ UserFree 函式

**<type> \_ UserFree** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。 Stub 會呼叫這個函式來釋放伺服器端的資料。 函式定義如下：

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

函 <type> 式名稱中的，表示在 **\[ 有線 \_ 封送 \]** 處理或 **\[ 使用者 \_ 封 \] 送** 處理類型定義中指定的 userm 類型。

*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。 旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。 下方的單字包含由 COM 通道所定義的封送處理內容旗標。 欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。

*PMyObj* 參數是使用者類型物件的指標。 NDR 引擎會釋放最上層物件。 您必須負責釋放最上層物件可能指向的任何物件。

必須在本機攔截和處理例外狀況，不能允許例外狀況 propigated 呼叫堆疊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封送處理使用者 \_ 封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 