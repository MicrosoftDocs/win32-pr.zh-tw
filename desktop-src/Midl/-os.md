---
title: /Os 參數
description: /Os 參數會指定混合模式方法，以封送處理在用戶端與伺服器之間傳遞的存根程式碼。
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /Os 參數 MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967860"
---
# <a name="os-switch"></a>/Os 參數

**/Os** 參數會指定混合模式方法，以封送處理在用戶端與伺服器之間傳遞的存根程式碼。

``` syntax
midl /Os
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

在決定封送處理常式代碼的方法之前，必須考慮一些重要的問題。 這些問題的大小和效能都有問題。 MIDL 編譯器提供兩種方法來封送處理常式代碼：混合模式 (**/os**) 和完整解釋 ([**/Oi**](-oi.md)) 。 完全解讀的方法會完全離線地封送處理資料。 這會大幅減少存根程式碼的大小，但它也會導致效能降低。

針對回溯相容性以外的所有用途，請使用 MIDL 預設模式 **/Oicf** /robust。 此模式是 MIDL 編譯器的安全標準模式;任何其他模式都應該只在仔細考慮安全性隱含的考慮之後才使用，以瞭解未來的延伸模組只會針對預設模式執行。 在混合模式中，編譯器會封送處理產生的存根中內嵌的一些參數。 雖然這會產生較大的存根大小，但它也可能會提供更高的效能。

MIDL 只會在 [**/Oicf**](-oi.md) 模式中提供多維陣列和多維度大小指標的完整支援。 在 **/os** 和 **/Oi** 模式中，編譯器支援簡單的案例，例如固定大小的陣列。 在 **/os** 或 **/Oi** 模式中使用多維陣列可能會導致未正確封送處理的參數。 當您的介面定義的參數是多維陣列或多維度大小的指標時，Microsoft 建議您使用 **/Oicf** 命令列參數。

為了進一步定義資料的封送處理方式層級，這個版本的 RPC 會提供 \[ [**optimize**](optimize.md) \] 屬性。 這個屬性是用來做為 ACF 介面屬性或 operation 屬性，以選取封送處理模式。

## <a name="examples"></a>範例

**midl/Os 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**優化**](optimize.md)
</dt> <dt>

[**/no \_ 格式 \_ 選擇**](-no-format-opt.md)
</dt> </dl>

 

 




