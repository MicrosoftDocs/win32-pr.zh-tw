---
description: 登錄值可以儲存各種格式的資料。
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: 登錄數值型別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849584"
---
# <a name="registry-value-types"></a><span data-ttu-id="570ae-103">登錄數值型別</span><span class="sxs-lookup"><span data-stu-id="570ae-103">Registry Value Types</span></span>

<span data-ttu-id="570ae-104">登錄值可以儲存各種格式的資料。</span><span class="sxs-lookup"><span data-stu-id="570ae-104">A registry value can store data in various formats.</span></span> <span data-ttu-id="570ae-105">當您在登錄值下儲存資料時（例如，藉由呼叫 [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) 函式），您可以指定下列其中一個值來表示要儲存的資料類型。</span><span class="sxs-lookup"><span data-stu-id="570ae-105">When you store data under a registry value, for instance by calling the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function, you can specify one of the following values to indicate the type of data being stored.</span></span> <span data-ttu-id="570ae-106">當您取得登錄值時，如 [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) 的函式會使用這些值來指出抓取的資料類型。</span><span class="sxs-lookup"><span data-stu-id="570ae-106">When you retrieve a registry value, functions such as [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) use these values to indicate the type of data retrieved.</span></span>

<span data-ttu-id="570ae-107">下列登錄數值型別定義于 Winnt. h 中。</span><span class="sxs-lookup"><span data-stu-id="570ae-107">The following registry value types are defined in Winnt.h.</span></span>



| <span data-ttu-id="570ae-108">值</span><span class="sxs-lookup"><span data-stu-id="570ae-108">Value</span></span>                                 | <span data-ttu-id="570ae-109">類型</span><span class="sxs-lookup"><span data-stu-id="570ae-109">Type</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="570ae-110">REG \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="570ae-110">REG\_BINARY</span></span><br/>                | <span data-ttu-id="570ae-111">任何形式的二進位資料，</span><span class="sxs-lookup"><span data-stu-id="570ae-111">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="570ae-112">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="570ae-112">REG\_DWORD</span></span><br/>                 | <span data-ttu-id="570ae-113">32位數位。</span><span class="sxs-lookup"><span data-stu-id="570ae-113">A 32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="570ae-114">REG DWORD 位元組由大到 \_ \_ 小 \_</span><span class="sxs-lookup"><span data-stu-id="570ae-114">REG\_DWORD\_LITTLE\_ENDIAN</span></span><br/> | <span data-ttu-id="570ae-115">以位元組由大到小的格式的32位數位。</span><span class="sxs-lookup"><span data-stu-id="570ae-115">A 32-bit number in little-endian format.</span></span><br/> <span data-ttu-id="570ae-116">Windows 的設計是在以位元組由小到大的電腦架構上執行。</span><span class="sxs-lookup"><span data-stu-id="570ae-116">Windows is designed to run on little-endian computer architectures.</span></span> <span data-ttu-id="570ae-117">因此，此值會 \_ 在 Windows 標頭檔中定義為 REG DWORD。</span><span class="sxs-lookup"><span data-stu-id="570ae-117">Therefore, this value is defined as REG\_DWORD in the Windows header files.</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="570ae-118">REG \_ DWORD \_ BIG \_ ENDIAN</span><span class="sxs-lookup"><span data-stu-id="570ae-118">REG\_DWORD\_BIG\_ENDIAN</span></span><br/>    | <span data-ttu-id="570ae-119">以位元組由大到小的格式的32位數位。</span><span class="sxs-lookup"><span data-stu-id="570ae-119">A 32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="570ae-120">某些 UNIX 系統支援位元組由大到小的架構。</span><span class="sxs-lookup"><span data-stu-id="570ae-120">Some UNIX systems support big-endian architectures.</span></span><br/>                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="570ae-121">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="570ae-121">REG\_EXPAND\_SZ</span></span><br/>            | <span data-ttu-id="570ae-122">以 null 終止的字串，其中包含環境變數的未展開參考 (例如 "% PATH%" ) 。</span><span class="sxs-lookup"><span data-stu-id="570ae-122">A null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="570ae-123">它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。</span><span class="sxs-lookup"><span data-stu-id="570ae-123">It will be a Unicode or ANSI string depending on whether you use the Unicode or ANSI functions.</span></span> <span data-ttu-id="570ae-124">若要展開環境變數參考，請使用 [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="570ae-124">To expand the environment variable references, use the [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function.</span></span><br/>                                                                                 |
| <span data-ttu-id="570ae-125">REG \_ 連結</span><span class="sxs-lookup"><span data-stu-id="570ae-125">REG\_LINK</span></span><br/>                  | <span data-ttu-id="570ae-126">以 null 終止的 Unicode 字串，其中包含以 REG [](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) \_ OPTION \_ CREATE link 呼叫 RegCreateKeyEx 函式所建立之符號連結的目標路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="570ae-126">A null-terminated Unicode string that contains the target path of a symbolic link that was created by calling the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function with REG\_OPTION\_CREATE\_LINK.</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="570ae-127">REG \_ 多重 \_ SZ</span><span class="sxs-lookup"><span data-stu-id="570ae-127">REG\_MULTI\_SZ</span></span><br/>             | <span data-ttu-id="570ae-128">以 null 結束的字串序列，以空字串 (\\ 0) 結束。</span><span class="sxs-lookup"><span data-stu-id="570ae-128">A sequence of null-terminated strings, terminated by an empty string (\\0).</span></span><br/> <span data-ttu-id="570ae-129">以下是一個範例：</span><span class="sxs-lookup"><span data-stu-id="570ae-129">The following is an example:</span></span><br/> <span data-ttu-id="570ae-130">*String1* \\0 *String2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0</span><span class="sxs-lookup"><span data-stu-id="570ae-130">*String1*\\0 *String2*\\0 *String3*\\0 *LastString*\\0\\0</span></span><br/> <span data-ttu-id="570ae-131">第一個 \\ 0 會終止第一個字串，最後一個0到最後一個字串的第二個會結束 \\ 最後一個字串，最後0則會 \\ 結束序列。</span><span class="sxs-lookup"><span data-stu-id="570ae-131">The first \\0 terminates the first string, the second to the last \\0 terminates the last string, and the final \\0 terminates the sequence.</span></span> <span data-ttu-id="570ae-132">請注意，最後的結束字元必須考慮到字串的長度。</span><span class="sxs-lookup"><span data-stu-id="570ae-132">Note that the final terminator must be factored into the length of the string.</span></span><br/> |
| <span data-ttu-id="570ae-133">REG \_ 無</span><span class="sxs-lookup"><span data-stu-id="570ae-133">REG\_NONE</span></span><br/>                  | <span data-ttu-id="570ae-134">沒有定義的實值型別。</span><span class="sxs-lookup"><span data-stu-id="570ae-134">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="570ae-135">REG \_ QWORD</span><span class="sxs-lookup"><span data-stu-id="570ae-135">REG\_QWORD</span></span><br/>                 | <span data-ttu-id="570ae-136">64位數位。</span><span class="sxs-lookup"><span data-stu-id="570ae-136">A 64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="570ae-137">REG \_ QWORD 位元組由大到 \_ 小 \_</span><span class="sxs-lookup"><span data-stu-id="570ae-137">REG\_QWORD\_LITTLE\_ENDIAN</span></span><br/> | <span data-ttu-id="570ae-138">以位元組由大到小的格式的64位數位。</span><span class="sxs-lookup"><span data-stu-id="570ae-138">A 64-bit number in little-endian format.</span></span><br/> <span data-ttu-id="570ae-139">Windows 的設計是在以位元組由小到大的電腦架構上執行。</span><span class="sxs-lookup"><span data-stu-id="570ae-139">Windows is designed to run on little-endian computer architectures.</span></span> <span data-ttu-id="570ae-140">因此，這個值 \_ 在 Windows 標頭檔中定義為 REG QWORD。</span><span class="sxs-lookup"><span data-stu-id="570ae-140">Therefore, this value is defined as REG\_QWORD in the Windows header files.</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="570ae-141">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="570ae-141">REG\_SZ</span></span><br/>                    | <span data-ttu-id="570ae-142">null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="570ae-142">A null-terminated string.</span></span> <span data-ttu-id="570ae-143">這會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。</span><span class="sxs-lookup"><span data-stu-id="570ae-143">This will be either a Unicode or an ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a><span data-ttu-id="570ae-144">字串值</span><span class="sxs-lookup"><span data-stu-id="570ae-144">String Values</span></span>

<span data-ttu-id="570ae-145">如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND \_ sz 型別，則字串可能尚未以適當的終止 null 字元儲存。</span><span class="sxs-lookup"><span data-stu-id="570ae-145">If data has the REG\_SZ, REG\_MULTI\_SZ, or REG\_EXPAND\_SZ type, the string may not have been stored with the proper terminating null characters.</span></span> <span data-ttu-id="570ae-146">因此，從登錄讀取字串時，您必須確定字串在使用之前已正確地終止;否則，它可能會覆寫緩衝區。</span><span class="sxs-lookup"><span data-stu-id="570ae-146">Therefore, when reading a string from the registry, you must ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="570ae-147"> (請注意，REG \_ 多重 \_ SZ 字串應該有兩個結束的 null 字元。 ) </span><span class="sxs-lookup"><span data-stu-id="570ae-147">(Note that REG\_MULTI\_SZ strings should have two terminating null characters.)</span></span>

<span data-ttu-id="570ae-148">將字串寫入登錄時，您必須指定字串的長度，包括結束的 null 字元 (\\ 0) 。</span><span class="sxs-lookup"><span data-stu-id="570ae-148">When writing a string to the registry, you must specify the length of the string, including the terminating null character (\\0).</span></span> <span data-ttu-id="570ae-149">常見的錯誤是使用 **strlen** 函式來判斷字串的長度，但請記住， **strlen** 只會傳回字串中的字元數，不包括終止的 null。</span><span class="sxs-lookup"><span data-stu-id="570ae-149">A common error is to use the **strlen** function to determine the length of the string, but to forget that **strlen** returns only the number of characters in the string, not including the terminating null.</span></span> <span data-ttu-id="570ae-150">因此，應計算字串的長度，如下所示： `strlen( string ) + 1`</span><span class="sxs-lookup"><span data-stu-id="570ae-150">Therefore, the length of the string should be calculated as follows: `strlen( string ) + 1`</span></span>

<span data-ttu-id="570ae-151">REG \_ 多重 \_ SZ 字串的結尾為長度為0的字串。</span><span class="sxs-lookup"><span data-stu-id="570ae-151">A REG\_MULTI\_SZ string ends with a string of length 0.</span></span> <span data-ttu-id="570ae-152">因此，序列中不能包含長度為零的字串。</span><span class="sxs-lookup"><span data-stu-id="570ae-152">Therefore, it is not possible to include a zero-length string in the sequence.</span></span> <span data-ttu-id="570ae-153">空的序列定義如下： \\ 0。</span><span class="sxs-lookup"><span data-stu-id="570ae-153">An empty sequence would be defined as follows: \\0.</span></span>

<span data-ttu-id="570ae-154">下列範例會逐步解說 REG \_ 多重 \_ SZ 字串。</span><span class="sxs-lookup"><span data-stu-id="570ae-154">The following example walks a REG\_MULTI\_SZ string.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a><span data-ttu-id="570ae-155">位元組格式</span><span class="sxs-lookup"><span data-stu-id="570ae-155">Byte Formats</span></span>

<span data-ttu-id="570ae-156">以 *位元組* 由小到大的格式來說，多位元組的值會儲存在記憶體中的最小位元組 (「小端」 ) 到最高的位元組。</span><span class="sxs-lookup"><span data-stu-id="570ae-156">In *little-endian format*, a multi-byte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="570ae-157">例如，值0x12345678 會儲存為 (0x78 0x56 0x34 0x12) 以位元組由小到大格式表示。</span><span class="sxs-lookup"><span data-stu-id="570ae-157">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span>

<span data-ttu-id="570ae-158">以 *位元組由大* 到小的格式來說，多重位元組值會儲存在記憶體中，從最高的位元組 ("big end" ) 到最小的位元組。</span><span class="sxs-lookup"><span data-stu-id="570ae-158">In *big-endian format*, a multi-byte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="570ae-159">例如，值0x12345678 會以位元組由大到小的格式儲存為 (0x12 0x34 0x56 0x78) 。</span><span class="sxs-lookup"><span data-stu-id="570ae-159">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span>

 

