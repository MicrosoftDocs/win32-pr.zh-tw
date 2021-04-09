---
title: /cpp_cmd 參數
description: /Cpp \_ cmd 參數會指定 MIDL 編譯器用來前置處理輸入檔的預處理器。
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd switch MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678664"
---
# <a name="cpp_cmd-switch"></a>/cpp \_ cmd 參數

**/Cpp \_ cmd** 參數會指定 MIDL 編譯器用來前置處理輸入檔的預處理器。

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*C \_ 預處理器 \_ 二進位檔* 
</dt> <dd>

指定叫用預處理器的命令。 此命令可讓開發人員覆寫預設的預處理器。 根據預設，MIDL 會從組建電腦的組建環境叫用 Microsoft C/c + + 編譯器。

</dd> </dl>

## <a name="remarks"></a>備註

參數的 *C \_ 預處理器 \_ 二進位* 引數可以指定完整路徑; exe 尾碼和引號是選擇性的。 一般情況下，開發人員會使用參數來選擇特定版本的 Microsoft C/c + + 預處理器或組建環境中的對等專案。 在此情況下，不需要搭配 **/cpp \_ cmd** 使用 [**/cpp \_ opt**](-cpp-opt.md)參數。

使用非 Microsoft 預處理器時，尤其是當指定的預處理器未將輸出導向至 stdout 時，必須指定將輸出重新導向至 stdout 的 C 編譯器參數，做為 MIDL 編譯器 [**/cpp \_ opt**](-cpp-opt.md) 參數的一部分。 如需詳細資料，請參閱[C-預處理器的 MIDL 需求](c-preprocessor-requirements-for-midl.md)

預處理器是透過 **/cpp \_ cmd**、 [**/cpp \_ opt**](-cpp-opt.md)、 [**/d**](-d.md)、 [**/i**](-i.md)和 [**/u**](-u.md) 參數提供給 MIDL 編譯器的資訊所組成的命令字串來叫用。 下表摘要說明如何針對 **/cpp \_ cmd** 和 **/cpp \_ opt** 參數的每個組合來建立命令字串。

未指定 **/cpp \_ cmd** 參數時，MIDL 編譯器會叫用 Microsoft C/c + + 編譯器。 MIDL 使用在組建環境中找到的 Cl.exe 二進位檔。

當 [**/cpp \_ opt**](-cpp-opt.md) 參數不存在時，midl 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 MIDL [**/i**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 選項所指定的資訊。 字串/E 也會串連至 C 編譯器調用字串，表示 C/c + + 編譯器只應執行前置處理。 已新增 [**/nologo**](-nologo.md) 參數來隱藏 C/c + + 編譯器橫幅。 MIDL 編譯器會使用串連的字串來叫用最上層 IDL 的 C 預處理器，以及匯入的 IDL 檔案，也會針對任何存在的對應 ACF 檔叫用。

如果有 [**/cpp \_ opt**](-cpp-opt.md) 參數存在（這應該是目前32位和64位平臺的罕見案例），MIDL 編譯器會將 **/cpp \_ cmd** 參數所指定的字串與 **/cpp \_ opt** 參數所指定的字串串連在一起。 MIDL 編譯器會使用串連的字串來叫用指定的預處理器二進位檔，以取代預設的預處理器。 當 **/cpp \_ opt** 參數存在時， [**/I**](-i.md)、 [**/D**](-d.md)和 [**/U**](-u.md) 參數指定的 MIDL 編譯器選項和 C 編譯器參數/e 都不會與字串串連。 您必須在字串中提供/E 選項或對等專案。



| /cpp \_ cmd 存在嗎？ | /cpp \_ opt 存在嗎？ | Description                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 無 (預設值)       | 無 (預設值)       | 使用從 MIDL [**/i**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 參數取得的設定，叫用預設的 Microsoft C/c + + 編譯器。 新增預處理器參數/E 和 [**/nologo**](-nologo.md)。 |
| 是                | 否                 | 使用與上述相同的參數叫用指定的預處理器二進位檔。                                                                                                                                        |
| 否                 | 是                | 使用指定的選項叫用 Microsoft C 編譯器。 不使用 MIDL [**/i**](-i.md)、 [**/d**](-d.md)、 [**/u**](-u.md) 選項。 您必須提供/E 作為 [**/cpp \_ opt**](-cpp-opt.md)的一部分。             |
| 是                | 是                | 只使用指定的選項叫用指定的預處理器二進位檔。 您必須使用引號。                                                                                                                       |



 

## <a name="examples"></a>範例

**midl/cpp \_ cmd d： \\ nt \\ tools \\ IA64 \\cl.exe/DFLAG = TRUE/Ic： \\ inc. 名稱 .idl**

**midl/cpp \_ cmd "mycpp"/DFLAG = TRUE/Ic： \\ inc. 檔案名 .idl**

**midl/cpp \_ opt "/E/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**

**midl/cpp \_ cmd "cl"/cpp \_ opt "/e/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[C-MIDL 的預處理器需求](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




