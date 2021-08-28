---
title: 標頭注釋
description: 標頭注釋描述函式如何使用其參數和傳回值。
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- WindowsAPI，標頭檔批註
- 標頭檔批註
- Specstrings。h
- '標準批註語言 (SAL) '
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ad560d00c45714d0feaa9ab2fa58ff4c985730fd563d4943ff028f561f2793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643628"
---
# <a name="header-annotations"></a>標頭注釋

\[本主題說明透過 Windows 7 Windows 標頭中支援的注釋。 如果您正在針對 Windows 8 進行開發，您應該使用[SAL 注釋]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120))中所述的注釋。\]

標頭注釋描述函式如何使用其參數和傳回值。 這些批註已新增至許多 Windows 標頭檔，以協助您確定您正確地呼叫 Windows API。 如果您啟用程式碼分析（從 Visual Studio 2005 開始提供），則編譯器將會產生層級6000警告，如果您未根據批註所描述的使用方式來呼叫這些函式。 您也可以在自己的程式碼中新增這些批註，以確保正確地呼叫它。 若要在 Visual Studio 中啟用程式碼分析，請參閱 Visual Studio 版本的檔。

這些批註是在 Specstrings 中定義。 它們建置於屬於標準批註語言一部分的基本專案， (SAL) 並使用執行 `_declspec("SAL_*")` 。

注釋有兩種類別：緩衝區注釋和先進注釋。

## <a name="buffer-annotations"></a>緩衝區批註

緩衝區批註描述函式如何使用其指標，並可用於偵測緩衝區溢位。 每個參數都可以使用零或一個緩衝區注釋。 緩衝區批註會以前置底線和下列各節所述的元件來建立。



| 緩衝區大小                                                                                  | 描述                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span> (*大小*) <br/>                        | 指定緩衝區的總大小。 搭配 \_ bcount 和 \_ ecount 使用; 請勿使用 with \_ 部分。 此值是可存取的空間;它可能小於配置的空間。<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span> (*大小*，*長度*) <br/> | 指定緩衝區的總大小和初始化長度。 搭配 \_ bcount \_ 元件和 \_ ecount 部分使用 \_ 。 總大小可能小於配置的空間。<br/>              |



 



| 緩衝區大小單位                                                       | 描述                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | 緩衝區大小以位元組為單位。<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | 緩衝區大小是在元素中。<br/> |



 



| 方向                                                            | Description                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_在<br/>          | 函數會從緩衝區讀取。 呼叫端會提供緩衝區，並將其初始化。<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_inout<br/> | 函數會從緩衝區讀取和寫入緩衝區。 呼叫端會提供緩衝區，並將其初始化。 如果與 deref 搭配使用 \_ ，緩衝區可能會由函式重新配置。<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_擴展<br/>       | 函數會寫入緩衝區。 如果用於傳回值或使用 \_ deref，則函式會提供緩衝區，並將其初始化。 否則，呼叫端會提供緩衝區，而函式會將它初始化。<br/> |



 



| 間接                                                                       | 描述                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_deref<br/>              | 取值參數以取得緩衝區指標。 此參數不可以是 **Null**。<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ opt<br/> | 取值參數以取得緩衝區指標。 此參數可以是 **Null**。<br/>     |



 



| 初始化                                                    | 描述                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_全<br/> | 函數會初始化整個緩衝區。 只能搭配輸出緩衝區使用。<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_部分<br/> | 此函式會初始化緩衝區的一部分，並明確地指出有多少。 只能搭配輸出緩衝區使用。<br/> |



 



| 必要或選擇性的緩衝區                                    | 描述                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_選擇<br/> | 此參數可以是 **Null**。<br/> |



 

下列範例會顯示 **GetModuleFileName** 函式的附注。 *HModule* 參數是選擇性的輸入參數。 *LpFilename* 參數是輸出參數;其大小（以字元為單位）是由 *nSize* 參數指定，其長度包括 **null** 終止字元。 *NSize* 參數是輸入參數。


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



以下是在 Specstrings 中定義的附注。 使用上述表格中的資訊來解讀其意義。

__bcount (*大小*)   
__bcount_opt (*大小*)   
__deref_bcount (*大小*)   
__deref_bcount_opt (*大小*)   
__deref_ecount (*大小*)   
__deref_ecount_opt (*大小*)   
__deref_in  
__deref_in_bcount (*大小*)   
__deref_in_bcount_opt (*大小*)   
__deref_in_ecount (*大小*)   
__deref_in_ecount_opt (*大小*)   
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*大小*)   
__deref_inout_bcount_full (*大小*)   
__deref_inout_bcount_full_opt (*大小*)   
__deref_inout_bcount_opt (*大小*)   
__deref_inout_bcount_part (*大小*，*長度*)   
__deref_inout_bcount_part_opt (*大小*，*長度*)   
__deref_inout_ecount (*大小*)   
__deref_inout_ecount_full (*大小*)   
__deref_inout_ecount_full_opt (*大小*)   
__deref_inout_ecount_opt (*大小*)   
__deref_inout_ecount_part (*大小*，*長度*)   
__deref_inout_ecount_part_opt (*大小*，*長度*)   
__deref_inout_opt  
__deref_opt_bcount (*大小*)   
__deref_opt_bcount_opt (*大小*)   
__deref_opt_ecount (*大小*)   
__deref_opt_ecount_opt (*大小*)   
__deref_opt_in  
__deref_opt_in_bcount (*大小*)   
__deref_opt_in_bcount_opt (*大小*)   
__deref_opt_in_ecount (*大小*)   
__deref_opt_in_ecount_opt (*大小*)   
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*大小*)   
__deref_opt_inout_bcount_full (*大小*)   
__deref_opt_inout_bcount_full_opt (*大小*)   
__deref_opt_inout_bcount_opt (*大小*)   
__deref_opt_inout_bcount_part (*大小*，*長度*)   
__deref_opt_inout_bcount_part_opt (*大小*，*長度*)   
__deref_opt_inout_ecount (*大小*)   
__deref_opt_inout_ecount_full (*大小*)   
__deref_opt_inout_ecount_full_opt (*大小*)   
__deref_opt_inout_ecount_opt (*大小*)   
__deref_opt_inout_ecount_part (*大小*，*長度*)   
__deref_opt_inout_ecount_part_opt (*大小*，*長度*)   
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*大小*)   
__deref_opt_out_bcount_full (*大小*)   
__deref_opt_out_bcount_full_opt (*大小*)   
__deref_opt_out_bcount_opt (*大小*)   
__deref_opt_out_bcount_part (*大小*，*長度*)   
__deref_opt_out_bcount_part_opt (*大小*，*長度*)   
__deref_opt_out_ecount (*大小*)   
__deref_opt_out_ecount_full (*大小*)   
__deref_opt_out_ecount_full_opt (*大小*)   
__deref_opt_out_ecount_opt (*大小*)   
__deref_opt_out_ecount_part (*大小*，*長度*)   
__deref_opt_out_ecount_part_opt (*大小*，*長度*)   
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*大小*)   
__deref_out_bcount_full (*大小*)   
__deref_out_bcount_full_opt (*大小*)   
__deref_out_bcount_opt (*大小*)   
__deref_out_bcount_part (*大小*，*長度*)   
__deref_out_bcount_part_opt (*大小*，*長度*)   
__deref_out_ecount (*大小*)   
__deref_out_ecount_full (*大小*)   
__deref_out_ecount_full_opt (*大小*)   
__deref_out_ecount_opt (*大小*)   
__deref_out_ecount_part (*大小*，*長度*)   
__deref_out_ecount_part_opt (*大小*，*長度*)   
__deref_out_opt  
__ecount (*大小*)   
__ecount_opt (*大小*)   
__in  
__in_bcount (*大小*)   
__in_bcount_opt (*大小*)   
__in_ecount (*大小*)   
__in_ecount_opt (*大小*)   
__in_opt  
__inout  
__inout_bcount (*大小*)   
__inout_bcount_full (*大小*)   
__inout_bcount_full_opt (*大小*)   
__inout_bcount_opt (*大小*)   
__inout_bcount_part (*大小*，*長度*)   
__inout_bcount_part_opt (*大小*，*長度*)   
__inout_ecount (*大小*)   
__inout_ecount_full (*大小*)   
__inout_ecount_full_opt (*大小*)   
__inout_ecount_opt (*大小*)   
__inout_ecount_part (*大小*，*長度*)   
__inout_ecount_part_opt (*大小*，*長度*)   
__inout_opt  
__out  
__out_bcount (*大小*)   
__out_bcount_full (*大小*)   
__out_bcount_full_opt (*大小*)   
__out_bcount_opt (*大小*)   
__out_bcount_part (*大小*，*長度*)   
__out_bcount_part_opt (*大小*，*長度*)   
__out_ecount (*大小*)   
__out_ecount_full (*大小*)   
__out_ecount_full_opt (*大小*)   
__out_ecount_opt (*大小*)   
__out_ecount_part (*大小*，*長度*)   
__out_ecount_part_opt (*大小*，*長度*)   
__out_opt  

## <a name="advanced-annotations"></a>Advanced 批註

Advanced 批註提供參數或傳回值的其他相關資訊。 每個參數或傳回值都可以使用零或一個 advanced 批註。



| Annotation                                                                                                                                               | 描述                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*資源*) <br/> | 函數會封鎖指定的資源。<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_回檔<br/>                                                                        | 函數可用來當做函式指標。<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | 呼叫端必須檢查傳回值。<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_格式 \_ 字串<br/>                                                        | 參數是包含 printf 樣式% 標記的字串。<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_在 \_ awcount (*運算式* 中，*大小*) <br/>                            | 如果在結束時運算式為 true，則會指定輸入緩衝區的大小（以位元組為單位）。 如果運算式為 false，則會在元素中指定大小。<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | 緩衝區最多可存取，包括兩個 **null** 字元或指標的第一個序列。<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated<br/>                                                      | 緩衝區最多可存取，並包括第一個 **null** 字元或指標。<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*，*size*) <br/>                         | 如果在結束時運算式為 true，則會指定輸出緩衝區的大小（以位元組為單位）。 如果運算式為 false，則會在元素中指定大小。 <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_覆蓋<br/>                                                                        | 指定虛擬方法的 c # 樣式覆寫行為。<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_保留<br/>                                                                        | 參數已保留供日後使用，且必須為零或 **Null**。<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success (*expr*) <br/>                                                       | 如果在結束時運算式為 true，則呼叫端可以依賴其他注釋所指定的所有保證。 如果運算式為 false，則呼叫端無法依賴保證。 這個批註會自動加入至傳回 **HRESULT** 值的函式。<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*ctype*) <br/>                                                    | 將參數視為指定的型別，而不是其宣告的型別。<br/>                                                                                                                                                                                             |



 

下列範例顯示 [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)、 [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)和 [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) 函數的緩衝區和先進注釋。


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[SAL 注釋](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[逐步解說：分析 C/C++ 程式碼的缺失](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

