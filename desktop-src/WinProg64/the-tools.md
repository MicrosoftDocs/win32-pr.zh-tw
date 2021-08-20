---
title: 工具
description: 本主題說明可供您用來讓應用程式64位就緒的工具。 Windows 10 適用于 x64 和 ARM64 型處理器。
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，工具
- 工具 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28084c445d664e130a9bb6dc5c087f8421cdaa5746845308258662739ee9084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569888"
---
# <a name="the-tools"></a>工具

本主題說明可供您用來讓應用程式64位就緒的工具。 Windows 10 適用于 x64 和 ARM64 型處理器。

## <a name="include-files"></a>包含檔案

在 32-和64位 Windows 之間，API 元素幾乎完全相同。 Windows 標頭檔已經過修改，因此可以同時用於32和64位的程式碼。 新的64位類型和宏會定義在新的標頭檔 Basetsd 中，它位於 Windows .h 所包含的標頭檔集中。 Basetsd 包含新的資料類型定義，可協助您使原始程式碼與單字大小無關。

## <a name="new-data-types"></a>新的資料類型

Windows 標頭檔包含新的資料類型。 這些類型主要用於與32位資料類型的類型相容性。 新的型別提供與現有類型完全相同的輸入，同時也提供64位 Windows 的支援。 如需詳細資訊，請參閱 [新的資料類型](the-new-data-types.md) 或 Basetsd .h 標頭檔。

## <a name="predefined-macros"></a>預先定義的巨集

編譯器會定義下列宏以識別平臺。



| 巨集   | 意義                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | 64位平臺。 這包括 x64 和 ARM64。                                                        |
| \_WIN32 | 32位平臺。 64位編譯器也會定義這個值，以提供回溯相容性。<br/> |
| \_WIN16 | 16位平臺                                                                                           |



 

以下是架構特有的宏。



| 巨集      | 意義                |
|------------|------------------------|
| \_M \_ IA64  | Intel Itanium 平臺 |
| \_M \_ IX86  | x86 平臺           |
| \_M \_ X64   | x64 平臺           |
| \_M \_ ARM64 | ARM64 平臺         |



 

請勿使用這些宏，但請 \_ 盡可能使用 WIN64、 \_ WIN32 和 WIN16 （但不含架構專屬程式碼） \_ 。

## <a name="helper-functions"></a>輔助函式

下列內嵌函式 (在 Basetsd 中定義) 可協助您安全地將值從某個類型轉換成另一個類型。

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> **IntToPtr** sign-擴充 **Int** 值、 **UIntToPtr** 零延伸不 **帶正負** 號的 int 值、 **LongToPtr** sign 擴充 **long** 值， **ULongToPtr** 零延伸不 **帶正負** 號的長整數值。

 

## <a name="64-bit-compiler"></a>64位編譯器

64位編譯器可以用來識別指標截斷、不當的型別轉換，以及其他64位特定的問題。

當編譯器第一次執行時，可能會產生許多指標截斷或類型不符的警告，如下所示：

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

使用這些警告作為指南，讓程式碼更健全。 最好的作法是消除所有警告，尤其是指標截斷警告。

## <a name="64-bit-compiler-switches-and-warnings"></a>64位編譯器參數和警告

請注意，此編譯器會啟用 LLP64 資料模型。

有警告選項可協助移植至 LLP64。 -Wp64-W3 參數會啟用下列警告：

-   C4305：截斷警告。 例如，「return」：從「不帶正負號的 int64」到「long」的截斷。
-   C4311：截斷警告。 例如，"type cast"：從 "int \* \_ ptr64" 到 "int" 的指標截斷。
-   C4312：轉換成較大大小的警告。 例如，「類型轉換」：從 "int" 轉換成 \* \_ 較大大小的 "int ptr64"。
-   C4318：傳遞零長度。 例如，將常數零當作長度傳遞給 **memset** 函數。
-   C4319： Not 運算子。 例如，"~"：零將「不帶正負號的 long」延伸至較大的「不帶正負號 \_ 的 int64」。
-   C4313：呼叫 **printf** 系列的函式，其中包含衝突的轉換類型規範和引數。 例如，格式字串中的 "printf"： "% p" 與類型 "int64" 的引數2衝突 \_ 。 另一個範例是呼叫 printf ( "% x"，指標 \_ 值) ; 這會造成最高32位的截斷。 正確的呼叫是 printf ( "% p"，指標 \_ 值) 。
-   C4244：與現有的警告 C4242 相同。 例如，「return」：從「int64」轉換 \_ 成「不帶正負號的整數」可能會遺失資料。

## <a name="64-bit-linker-and-libraries"></a>64位連結器和程式庫

若要建立應用程式，請使用 Windows SDK 所提供的連結器和程式庫。 大部分的32位程式庫都有相對應的64位版本，但某些舊版程式庫只有在32位版本中才可使用。 針對64位 Windows 建立應用程式時，呼叫這些程式庫的程式碼將不會連結。

 

 





