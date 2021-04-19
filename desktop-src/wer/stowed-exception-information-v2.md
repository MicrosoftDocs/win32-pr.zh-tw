---
title: STOWED_EXCEPTION_INFORMATION_V2 結構
description: 包含 stowed 例外狀況資訊。
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 結構 Windows 錯誤報告
- PSTOWED_EXCEPTION_INFORMATION_V2 結構指標 Windows 錯誤報告
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966531"
---
# <a name="stowed_exception_information_v2-structure"></a>STOWED \_ 例外狀況 \_ 資訊 \_ V2 結構

包含 stowed 例外狀況資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>成員

<dl> <dt>

**標頭**
</dt> <dd>

類型： **[ **STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**](stowed-exception-information-header.md)**

</dd> <dd>

[**STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**](stowed-exception-information-header.md)結構，包含此父結構的資訊。

</dd> <dt>

**ResultCode**
</dt> <dd>

類型： **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Stowed 例外狀況的 [**HRESULT**](/windows/desktop/WinProg/windows-data-types) 程式碼。

</dd> <dt>

**ExceptionForm**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

識別例外狀況形式的2位值。



| 值                                                                                                                                                                                                                                                                  | 意義                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**STOWED \_例外狀況 \_ 表單 \_ 二進位**</dt> <dt>0x01</dt> </dl> | 此值表示例外狀況的格式為二進位。<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**STOWED \_例外狀況 \_ 表單 \_ 文字**</dt> <dt>0x02</dt> </dl>       | 這個值表示例外狀況的格式是文字。<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

表示引發例外狀況之執行緒的30位值。 值會在儲存時右移至2個位。 若要將它轉換回有效的執行緒識別碼，請將值向左移位2。 例如：

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

 (*未命名的結構*) 
</dt> <dd>

只有當 **ExceptionForm** 成員設定為 **STOWED \_ 例外狀況 \_ 表單 \_ 二進位** 時，此嵌套結構的成員才有效。

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

包含例外狀況位址的指標。

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**StackTrace** 成員指向之堆疊追蹤中每個單字的大小（以位元組為單位）。 若為32位平臺，此值會設為4，64位平臺則設為8。

</dd> <dt>

**StackTraceWords**
</dt> <dd>

類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**StackTrace** 成員指向之堆疊追蹤中的文字數目。 單字數目等於陣列中的元素數目。

</dd> <dt>

**StackTrace**
</dt> <dd>

類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

包含堆疊追蹤之記憶體區塊的指標。

</dd> </dl> </dd> <dt>

 (*未命名的結構*) 
</dt> <dd>

只有當 **ExceptionForm** 成員設定為 **STOWED \_ 例外狀況 \_ 表單 \_ 文字** 時，此嵌套結構的成員才有效。

<dl> <dt>

**ErrorText**
</dt> <dd>

類型： **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

以 null 結束的字串指標，其中包含例外狀況的錯誤文字。

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指定 **NestedException** 成員指向之物件類型的32位值。 使用此位元組交換類型定義宏來定義值，該宏假設為位元組由小到小：

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

以下是一些常見的類型定義：



| 值                                                                                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ NONE**</dt> <dt> (0x00000000)</dt> </dl>                                  | 此值指定沒有任何嵌套的例外狀況物件。<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ WIN32**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' W32E ' )</dt> </dl>    | 這個值會指定 **NestedException** 成員指向 [**例外狀況 \_ 記錄**](/windows/desktop/api/winnt/ns-winnt-exception_record) 物件。<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ STOWED**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' STOW ' )</dt> </dl> | 這個值會指定 **NestedException** 成員指向另一個 stowed 例外狀況物件。 其他 stowed 例外狀況物件可以是 **stowed \_ 例外狀況 \_ 資訊 \_ V2** 物件或具有有效 **標頭** 成員的不同版本，也就是包含有效 [**Stowed 例外狀況 \_ \_ 資訊 \_ 標**](stowed-exception-information-header.md)頭的 **標頭** 成員。<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ CLR**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' CLR1 ' )</dt> </dl>          | 這個值會指定 **NestedException** 成員指向 ' CLR1 ' 例外狀況物件。<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**STOWED \_例外狀況 \_ 嵌套 \_ 類型 \_ LEO**</dt> <dt>STOWED 例外狀況 \_ \_ 嵌套 \_ 類型 ( ' LEO1 ' )</dt> </dl>          | 這個值會指定 **NestedException** 成員指向語言例外狀況物件。<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**NestedException**
</dt> <dd>

類型： **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

嵌套例外狀況類型的指標。 物件的類型是由 **NestedExceptionType** 成員所表示。

</dd> </dl>

## <a name="remarks"></a>備註

**STOWED \_例外狀況 \_ 資訊 \_ V2** 和 [**STOWED 例外狀況 \_ \_ 資訊 \_ 標頭**](stowed-exception-information-header.md) 目前未定義于可公開取得的標頭中，因此您必須先在原始程式碼中定義它們，然後才能使用它們。

**STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構與此結構相同，但不包含 **NestedExceptionType** 和 **NestedException** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                         |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**例外狀況 \_ 記錄**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**STOWED \_ 例外狀況 \_ 資訊 \_ 標頭**](stowed-exception-information-header.md)
</dt> </dl>

 

