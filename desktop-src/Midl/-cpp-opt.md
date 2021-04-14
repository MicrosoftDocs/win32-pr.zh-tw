---
title: /cpp_opt 參數
description: /Cpp \_ opt 參數指定要傳遞至 c/c + + 預處理器的選項。
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt switch MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383405"
---
# <a name="cpp_opt-switch"></a>/cpp \_ opt 參數

**/Cpp \_ opt** 參數指定要傳遞至 c/c + + 預處理器的選項。

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*C \_ 預處理器 \_ 選項* 
</dt> <dd>

指定與叫用預處理器相關聯的命令列選項。 

**注意**：針對 Microsoft C/c + + 預處理器，您必須提供 `/E` 參數作為 *C \_ 預處理器 \_ 選項* 字串的一部分。 

使用一個以上的選項時，以及針對空格，都需要引號。

</dd> </dl>

## <a name="remarks"></a>備註

除非有特定原因需要這麼做，否則請勿使用此參數。 如需有關前置處理的重要資訊，請參閱 [MIDL 的 C 預處理器需求](c-preprocessor-requirements-for-midl.md) 。

**/Cpp \_ opt** 參數可以搭配或不搭配 [**/cpp \_ cmd**](-cpp-cmd.md)參數使用。 請參閱 **/cpp \_ cmd** ，以取得在任一情況下如何建立預處理器命令列的詳細資料。

**/Cpp \_ opt** 參數（如果有指定）必須一律包含，才能 `/E` 正確運作。

## <a name="examples"></a>範例

**midl/cpp \_ cmd d： \\ nt \\ tools \\ IA64 \\cl.exe/DFLAG = TRUE/Ic： \\ inc. 名稱 .idl**

**midl/cpp \_ cmd "mycpp"/DFLAG = TRUE/Ic： \\ inc. 檔案名 .idl**

**midl/cpp \_ opt "/E/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**

**midl/cpp \_ cmd "cl"/cpp \_ opt "/e/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[C-MIDL 的預處理器需求](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




