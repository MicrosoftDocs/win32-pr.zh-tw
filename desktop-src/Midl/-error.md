---
title: /error 參數
description: /Error 參數會決定產生的存根會在執行時間執行的錯誤檢查類型。
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /error 參數 MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7af27de3d83171c8f1f89d0b860bf0b38ddfb6639a12bf40f90a58f06a273cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105628"
---
# <a name="error-switch"></a>/error 參數

**/Error** 參數會決定產生的存根會在執行時間執行的錯誤檢查類型。

> [!Note]  
> 這項功能已淘汰，不再支援。 建議使用 [**/robust**](-robust.md) 參數。

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>配置 * * * *


</dt> <dd>

檢查 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 是否傳回 **Null** 值，指出記憶體不足的錯誤。

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>存根 \_ 資料 * * * *


</dt> <dd>

產生存根來攔截伺服器端的解除封送例外狀況，並將它們傳播回用戶端。

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>ref * * * *


</dt> <dd>

產生在執行時間執行檢查的程式碼，以確保不會將 **Null** 參考指標傳遞至用戶端存根，並且 \_ 在找到任何時引發 RPC X \_ Null \_ REF \_ 指標例外狀況。

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>界限 \_ 檢查 * * * *


</dt> <dd>

根據傳輸長度規格，檢查一致且不同陣列的大小。

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>無 * * * *


</dt> <dd>

不執行錯誤檢查。

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>全部 * * * *


</dt> <dd>

執行所有錯誤檢查。 自 MIDL 5.0 版起，這是預設的編譯器參數。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**/Error** 參數會選取產生的存根檔案將執行的錯誤檢查數目。 自 MIDL 5.0 版起，預設設定為 [ **全部/error**]。

預設會在所有 MIDL) 版本中 (檢查的列舉錯誤，都是在 **列舉型別** (32 位整數) 和 **簡短列舉** 型別之間轉換時所造成的截斷錯誤， (列舉的網路資料 [**表示) ，**](enum.md) 以及列舉中超過32767的識別碼數目。

在所有 MIDL) 的版本中，預設也 (記憶體存取錯誤檢查，適用于超過封送處理常式代碼中緩衝區結尾的指標，以及其大小小於零的符合標準陣列。 使用 **/error 界限 \_ 檢查** 旗標來檢查是否有其他不正確陣列界限。

當您指定 **/error 配置** 時，存根會包含程式碼，當 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 傳回0時，就會引發例外狀況。

**/Error 存根 \_ data** 選項可防止用戶端資料在封送處理期間使伺服器損毀，並有效提供更健全的方法來處理封送處理作業。

自 Windows 2000 起，基礎執行時間 NDR 封送處理引擎會執行大部分的檢查。 這表示，如果您使用其中一個完整解釋的模式 ([**/Oi**](-oi.md)， **/Oif**) 的存根產生，選擇不同的錯誤檢查選項將不會對效能造成影響。

## <a name="examples"></a>範例

**midl/error 設定檔名 .idl**

**midl/error 無檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




