---
description: 深入瞭解： JET_USERDEFINEDDEFAULT 結構
title: JET_USERDEFINEDDEFAULT 結構
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000183"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="dcf16-103">JET_USERDEFINEDDEFAULT 結構</span><span class="sxs-lookup"><span data-stu-id="dcf16-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="dcf16-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dcf16-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="dcf16-105">JET_USERDEFINEDDEFAULT 結構</span><span class="sxs-lookup"><span data-stu-id="dcf16-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="dcf16-106">**JET_USERDEFINEDDEFAULT** 結構會與 JET_bitColumnUserDefinedDefault 一起指定，以提供新的資料行使用回呼決定的預設值。</span><span class="sxs-lookup"><span data-stu-id="dcf16-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="dcf16-107">這項技術可以用來執行計算的資料行。</span><span class="sxs-lookup"><span data-stu-id="dcf16-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="dcf16-108">**WINDOWS XP：** 在 Windows XP 中引進 **JET_USERDEFINEDDEFAULT** 結構。</span><span class="sxs-lookup"><span data-stu-id="dcf16-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="dcf16-109">成員</span><span class="sxs-lookup"><span data-stu-id="dcf16-109">Members</span></span>

<span data-ttu-id="dcf16-110">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="dcf16-110">**szCallback**</span></span>

<span data-ttu-id="dcf16-111">以 "module function" 格式執行回呼的函式的匯出名稱 \! 。</span><span class="sxs-lookup"><span data-stu-id="dcf16-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="dcf16-112">回呼會保存為數據行架構的一部分。</span><span class="sxs-lookup"><span data-stu-id="dcf16-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="dcf16-113">函數的實際主機可執行檔和匯出名稱必須保存，才能在執行時間查閱函數的真真實位址。</span><span class="sxs-lookup"><span data-stu-id="dcf16-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="dcf16-114">模組名稱是包含函數的主機二進位檔名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf16-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="dcf16-115">函數名稱是該函式的匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf16-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="dcf16-116">資料庫引擎會在執行時間使用這兩項資訊來找出回呼的真正位址，方法是對模組名稱執行 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 呼叫，然後在函式名稱後面加上 [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="dcf16-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="dcf16-117">例如，如果回呼是在稱為 MyCallback.DLL 的 DLL 中執行，而且該 DLL 儲存在 C： MyApplication 中，而且實回檔的函式 \\ 從 DLL 匯出為 UserDefinedDefaultCallback，則所需的字串會是 "C： \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback"。</span><span class="sxs-lookup"><span data-stu-id="dcf16-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="dcf16-118">**注意**  Embedded " \! "</span><span class="sxs-lookup"><span data-stu-id="dcf16-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="dcf16-119">不支援回呼名稱的模組部分中的字元。</span><span class="sxs-lookup"><span data-stu-id="dcf16-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="dcf16-120">強烈建議您使用不是主機架構功能的回呼名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf16-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="dcf16-121">例如，請勿使用裝飾為 stdcall () 的匯出， UserDefinedDefaultCallback@32 因為只有 x86 電腦才支援此呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="dcf16-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="dcf16-122">如果使用這類回呼，則資料庫只能在 x86 電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="dcf16-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="dcf16-123">在此情況下，您應該使用別名來建立平臺中立的匯出。</span><span class="sxs-lookup"><span data-stu-id="dcf16-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="dcf16-124">強烈建議您使用正在執行回呼的模組名稱的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dcf16-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="dcf16-125">如果使用相對路徑，則裝載資料庫的進程可能會受到惡意二進位檔的攻擊。</span><span class="sxs-lookup"><span data-stu-id="dcf16-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="dcf16-126">應用程式應該只傳遞受信任的回呼給 database engine。</span><span class="sxs-lookup"><span data-stu-id="dcf16-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="dcf16-127">資料庫引擎會載入二進位檔，以在建立相關聯的資料行時驗證它是否存在。</span><span class="sxs-lookup"><span data-stu-id="dcf16-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="dcf16-128">如果二進位檔的路徑未經過驗證或知道被信任，則可能會攻擊裝載資料庫的進程。</span><span class="sxs-lookup"><span data-stu-id="dcf16-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="dcf16-129">**pbUserData**</span><span class="sxs-lookup"><span data-stu-id="dcf16-129">**pbUserData**</span></span>

<span data-ttu-id="dcf16-130">當叫用時，要傳遞至回呼的使用者定義資料的獨立區塊。提供的資料區塊將會保存為數據行架構的一部分。</span><span class="sxs-lookup"><span data-stu-id="dcf16-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="dcf16-131">如此一來，資料區塊必須完全獨立，而且無法參考資料庫範圍以外的任何資料。</span><span class="sxs-lookup"><span data-stu-id="dcf16-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="dcf16-132">如果 **pbUserData** 為零，則會忽略 **cbUserData** 的值。</span><span class="sxs-lookup"><span data-stu-id="dcf16-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="dcf16-133">在此情況下，當叫用時，不會將使用者定義資料傳遞至回呼。</span><span class="sxs-lookup"><span data-stu-id="dcf16-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="dcf16-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="dcf16-134">**cbUserData**</span></span>

<span data-ttu-id="dcf16-135">請參閱 **pbUserData**。</span><span class="sxs-lookup"><span data-stu-id="dcf16-135">See **pbUserData**.</span></span>

<span data-ttu-id="dcf16-136">**szDependantColumns**</span><span class="sxs-lookup"><span data-stu-id="dcf16-136">**szDependantColumns**</span></span>

<span data-ttu-id="dcf16-137">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="dcf16-137">Reserved for future use.</span></span>

<span data-ttu-id="dcf16-138">這個成員應該一律設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="dcf16-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="dcf16-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcf16-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcf16-140"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="dcf16-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dcf16-141">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="dcf16-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcf16-142"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="dcf16-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dcf16-143">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="dcf16-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcf16-144"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="dcf16-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dcf16-145">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="dcf16-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcf16-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="dcf16-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="dcf16-147">實作為 <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) 和 <strong>JET_</strong> USERDEFINEDDEFAULT_A (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="dcf16-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="dcf16-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcf16-148">See Also</span></span>

[<span data-ttu-id="dcf16-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="dcf16-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="dcf16-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="dcf16-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="dcf16-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="dcf16-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
