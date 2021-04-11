---
title: /I 參數
description: /I 參數會指定要搜尋匯入之 IDL 檔案的目錄、包含的標頭檔和 ACF 檔。
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I 參數 MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022570"
---
# <a name="i-switch"></a>/I 參數

**/I** 參數會指定要搜尋匯入之 IDL 檔案的目錄、包含的標頭檔和 ACF 檔。

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*包含 \_ 路徑* 
</dt> <dd>

指定包含匯入、包含和 ACF 檔案的一或多個目錄。 **/I** 參數和 *include \_ 路徑* 之間的空格是選擇性的。 以分號字元 ( 分隔多個目錄，) 。

</dd> </dl>

## <a name="remarks"></a>備註

每個 **/i** 參數可以出現一個以上的目錄，而且每個 MIDL 編譯器調用可以出現一個以上的 **/i** 參數。 系統會依照指定的順序來搜尋目錄。

**/I** 參數設定也會由 MIDL 編譯器傳遞到 c 編譯器的 c 預處理器。 當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 **/i**、 [**/d**](-d.md)和 [**/U**](-u.md) 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。 當指定 MIDL 編譯器參數 **/no \_ cpp** 或 **/cpp \_ opt** 時，不會將 midl 編譯器參數 **/i** 傳遞給預處理器。

在 Microsoft 作業系統環境中 (64 位 Windows、32位 windows、16位 Windows 和 MS-DOS) ，會以下列順序搜尋目錄：

1.  目前的目錄
2.  **/I** 參數所指定的目錄會依參數遵循參數的順序 () 
3.  INCLUDE 環境變數所指定的目錄

使用 **/i** 參數指定目錄時， [**/no \_ def \_ idir**](-no-def-idir.md) 參數會指示 MIDL 編譯器忽略目前的目錄、忽略 INCLUDE 環境變數所指定的目錄，並只搜尋指定的目錄。

使用 **/i** 參數指定目錄時， [**/no \_ def \_ idir**](-no-def-idir.md) 參數會指示 MIDL 編譯器只搜尋目前目錄。

## <a name="examples"></a>範例

**midl/I c： \\ include; c： \\ include \\ h/i \\ include2 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




