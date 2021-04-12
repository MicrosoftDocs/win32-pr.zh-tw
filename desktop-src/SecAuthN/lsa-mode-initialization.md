---
description: 當電腦系統啟動時，「本地安全機構」 (LSA) 會自動將所有已註冊的安全性支援提供者/驗證套件 (SSP/AP) Dll 載入其進程空間中。 下圖顯示初始化處理常式。
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: LSA 模式初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513821"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="0b511-104">LSA 模式初始化</span><span class="sxs-lookup"><span data-stu-id="0b511-104">LSA Mode Initialization</span></span>

<span data-ttu-id="0b511-105">當電腦系統啟動時，「[*本地安全機構*](../secgloss/l-gly.md)」 (LSA) 會自動將所有已註冊的 [*安全性支援提供者*](../secgloss/s-gly.md) / [*驗證套件*](../secgloss/a-gly.md) (SSP/AP) dll 載入其進程空間中。</span><span class="sxs-lookup"><span data-stu-id="0b511-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="0b511-106">下圖顯示初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="0b511-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="0b511-107">"Kerberos" 代表 Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/ap，而「我的 SSP/ap」表示包含兩個自訂安全性封裝的自訂 SSP/ap。</span><span class="sxs-lookup"><span data-stu-id="0b511-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![lsa 模式初始化](images/lsamode1.png)

<span data-ttu-id="0b511-109">在啟動時，LSA 會在每個 SSP/AP 中呼叫 [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) 函式，以取得 DLL 中每個 [*安全性套件*](../secgloss/s-gly.md) 所執行之函式的指標。</span><span class="sxs-lookup"><span data-stu-id="0b511-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="0b511-110">函數指標會傳遞至 SECPKG 函式 [**\_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) 結構陣列中的 LSA。</span><span class="sxs-lookup"><span data-stu-id="0b511-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![lsa 呼叫 splsamodeinitialize 來取得函式指標](images/lsamode2.png)

<span data-ttu-id="0b511-112">收到 SECPKG 函式 [**\_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) 結構的集合之後，LSA 會呼叫每個安全性封裝的 [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) 函式。</span><span class="sxs-lookup"><span data-stu-id="0b511-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="0b511-113">LSA 會使用這個函式呼叫，將 Lsa SECPKG 函式 [**\_ \_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) 結構（其中包含可供安全性封裝使用的 lsa 支援函式的指標）傳遞給每個安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="0b511-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="0b511-114">除了將指標儲存至 LSA 支援函式之外，自訂安全性封裝應該使用其 **SpInitialize** 函式的實執行任何初始化相關的處理。</span><span class="sxs-lookup"><span data-stu-id="0b511-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="0b511-115">如需可供 LSA 模式安全性封裝使用的 LSA 支援函式清單，請參閱 [SSP/ap 所呼叫的 Lsa 函數](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0b511-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="0b511-116">如需註冊 SSP/AP DLL 的詳細資訊，請參閱 [註冊 ssp/ap](registering-ssp-ap-dlls.md)dll。</span><span class="sxs-lookup"><span data-stu-id="0b511-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
