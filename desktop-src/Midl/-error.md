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
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373236"
---
# <a name="error-switch"></a><span data-ttu-id="08999-104">/error 參數</span><span class="sxs-lookup"><span data-stu-id="08999-104">/error switch</span></span>

<span data-ttu-id="08999-105">**/Error** 參數會決定產生的存根會在執行時間執行的錯誤檢查類型。</span><span class="sxs-lookup"><span data-stu-id="08999-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="08999-106">這項功能已淘汰，不再支援。</span><span class="sxs-lookup"><span data-stu-id="08999-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="08999-107">建議使用 [**/robust**](-robust.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="08999-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="08999-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="08999-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="08999-109"><span id="allocation"></span><span id="ALLOCATION"></span>配置 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-110">檢查 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 是否傳回 **Null** 值，指出記憶體不足的錯誤。</span><span class="sxs-lookup"><span data-stu-id="08999-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="08999-111"><span id="stub_data"></span><span id="STUB_DATA"></span>存根 \_ 資料 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-112">產生存根來攔截伺服器端的解除封送例外狀況，並將它們傳播回用戶端。</span><span class="sxs-lookup"><span data-stu-id="08999-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="08999-113"><span id="ref"></span><span id="REF"></span>ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-114">產生在執行時間執行檢查的程式碼，以確保不會將 **Null** 參考指標傳遞至用戶端存根，並且 \_ 在找到任何時引發 RPC X \_ Null \_ REF \_ 指標例外狀況。</span><span class="sxs-lookup"><span data-stu-id="08999-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="08999-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>界限 \_ 檢查 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-116">根據傳輸長度規格，檢查一致且不同陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="08999-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="08999-117"><span id="none"></span><span id="NONE"></span>無 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-118">不執行錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="08999-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="08999-119"><span id="all"></span><span id="ALL"></span>全部 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="08999-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="08999-120">執行所有錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="08999-120">Performs all error checking.</span></span> <span data-ttu-id="08999-121">自 MIDL 5.0 版起，這是預設的編譯器參數。</span><span class="sxs-lookup"><span data-stu-id="08999-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08999-122">備註</span><span class="sxs-lookup"><span data-stu-id="08999-122">Remarks</span></span>

<span data-ttu-id="08999-123">**/Error** 參數會選取產生的存根檔案將執行的錯誤檢查數目。</span><span class="sxs-lookup"><span data-stu-id="08999-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="08999-124">自 MIDL 5.0 版起，預設設定為 [ **全部/error**]。</span><span class="sxs-lookup"><span data-stu-id="08999-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="08999-125">預設會在所有 MIDL) 版本中 (檢查的列舉錯誤，都是在 **列舉型別** (32 位整數) 和 **簡短列舉** 型別之間轉換時所造成的截斷錯誤， (列舉的網路資料 [**表示) ，**](enum.md) 以及列舉中超過32767的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="08999-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="08999-126">在所有 MIDL) 的版本中，預設也 (記憶體存取錯誤檢查，適用于超過封送處理常式代碼中緩衝區結尾的指標，以及其大小小於零的符合標準陣列。</span><span class="sxs-lookup"><span data-stu-id="08999-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="08999-127">使用 **/error 界限 \_ 檢查** 旗標來檢查是否有其他不正確陣列界限。</span><span class="sxs-lookup"><span data-stu-id="08999-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="08999-128">當您指定 **/error 配置** 時，存根會包含程式碼，當 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 傳回0時，就會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="08999-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="08999-129">**/Error 存根 \_ data** 選項可防止用戶端資料在封送處理期間使伺服器損毀，並有效提供更健全的方法來處理封送處理作業。</span><span class="sxs-lookup"><span data-stu-id="08999-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="08999-130">自 Windows 2000 起，基礎執行時間 NDR 封送處理引擎會執行大部分的檢查。</span><span class="sxs-lookup"><span data-stu-id="08999-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="08999-131">這表示，如果您使用其中一個完整解釋的模式 ([**/Oi**](-oi.md)， **/Oif**) 的存根產生，選擇不同的錯誤檢查選項將不會對效能造成影響。</span><span class="sxs-lookup"><span data-stu-id="08999-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="08999-132">範例</span><span class="sxs-lookup"><span data-stu-id="08999-132">Examples</span></span>

<span data-ttu-id="08999-133">**midl/error 設定檔名 .idl**</span><span class="sxs-lookup"><span data-stu-id="08999-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="08999-134">**midl/error 無檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="08999-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="08999-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08999-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08999-136">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="08999-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="08999-137">**/robust**</span><span class="sxs-lookup"><span data-stu-id="08999-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




