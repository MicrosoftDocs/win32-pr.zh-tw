---
description: 包含回呼函式的指標，這些函式可供密碼編譯服務提供者 (CSP) 函式使用。
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: 'VTableProvStruc 結構 (Cspdk .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694947"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="f5d27-103">VTableProvStruc 結構</span><span class="sxs-lookup"><span data-stu-id="f5d27-103">VTableProvStruc structure</span></span>

<span data-ttu-id="f5d27-104">**VTableProvStruc** 結構包含回呼函式的指標，可供 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="f5d27-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d27-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5d27-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="f5d27-106">成員</span><span class="sxs-lookup"><span data-stu-id="f5d27-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5d27-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="f5d27-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-108">表示結構版本的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="f5d27-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="f5d27-109">使用這個結構的三個版本。</span><span class="sxs-lookup"><span data-stu-id="f5d27-109">Three versions of this structure are used.</span></span> <span data-ttu-id="f5d27-110">版本為數字1、2和3，並決定結構的哪些成員有效。</span><span class="sxs-lookup"><span data-stu-id="f5d27-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="f5d27-111">第1版的成員在所有支援此結構的系統上都有效。</span><span class="sxs-lookup"><span data-stu-id="f5d27-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="f5d27-112">這是第1版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-113">**FuncVerifyImage**</span><span class="sxs-lookup"><span data-stu-id="f5d27-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-114">[**FuncVerifyImage**](funcverifyimage.md)回呼函式的位址，csp 會使用此函式來驗證 csp 將載入之任何 dll 的簽章。</span><span class="sxs-lookup"><span data-stu-id="f5d27-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="f5d27-115">CSP 進行函式呼叫的所有輔助 Dll 都必須以相同的方式進行簽署， (以及與主要 CSP DLL) 的金鑰相同。</span><span class="sxs-lookup"><span data-stu-id="f5d27-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="f5d27-116">若要確保這個簽章，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式，以動態方式載入輔助 dll。</span><span class="sxs-lookup"><span data-stu-id="f5d27-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="f5d27-117">但是在載入 DLL 之前，必須先驗證 DLL 的簽章。</span><span class="sxs-lookup"><span data-stu-id="f5d27-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="f5d27-118">CSP 會藉由呼叫 **FuncVerifyImage** 函式來執行這項驗證，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f5d27-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="f5d27-119">您可以儲存並使用這個函式指標，直到發行 CSP 內容為止。</span><span class="sxs-lookup"><span data-stu-id="f5d27-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="f5d27-120">這是第1版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-121">**FuncReturnhWnd**</span><span class="sxs-lookup"><span data-stu-id="f5d27-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-122">[**FuncReturnhWnd**](funcreturnhwnd.md)回呼函式的位址，這個函式會傳回 CSP 應使用的視窗控制碼做為顯示之任何使用者介面的父系或擁有者。</span><span class="sxs-lookup"><span data-stu-id="f5d27-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="f5d27-123">未直接與使用專用硬體的使用者和 Csp 通訊的 Csp 可以忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="f5d27-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="f5d27-124">此視窗控制碼預設為零，但應用程式可以使用 [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) 函式設定 **PP \_ 用戶端 \_ HWND** 屬性，將此值設定為不同的值。</span><span class="sxs-lookup"><span data-stu-id="f5d27-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="f5d27-125">您可以儲存並使用這個函式指標，直到發行 CSP 內容為止。</span><span class="sxs-lookup"><span data-stu-id="f5d27-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="f5d27-126">這是第1版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-127">**dwProvType**</span><span class="sxs-lookup"><span data-stu-id="f5d27-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-128">**DWORD** 值，指定要取得的提供者類型。</span><span class="sxs-lookup"><span data-stu-id="f5d27-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="f5d27-129">下列 [*提供者類型*](../secgloss/p-gly.md) 已預先定義，並會在 [CSP 互通性](https://www.bing.com/search?q=CSP+Interoperability)中詳細討論：</span><span class="sxs-lookup"><span data-stu-id="f5d27-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="f5d27-130">>PROV \_ RSA \_ FULL</span><span class="sxs-lookup"><span data-stu-id="f5d27-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="f5d27-131">>PROV \_ RSA \_ SIG</span><span class="sxs-lookup"><span data-stu-id="f5d27-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="f5d27-132">>PROV \_ DSS</span><span class="sxs-lookup"><span data-stu-id="f5d27-132">PROV\_DSS</span></span>
-   <span data-ttu-id="f5d27-133">>PROV \_ FORTEZZA</span><span class="sxs-lookup"><span data-stu-id="f5d27-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="f5d27-134">>PROV \_ MS \_ EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="f5d27-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="f5d27-135">這是第2版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-136">**pbCoNtextInfo**</span><span class="sxs-lookup"><span data-stu-id="f5d27-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-137">內容資訊陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="f5d27-137">A pointer to an array of context information.</span></span> <span data-ttu-id="f5d27-138">**PbCoNtextInfo** 和 **cbCoNtextInfo** 成員一起決定使用 PP 內容資訊集呼叫 [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**)函式時所使用的資訊集 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5d27-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="f5d27-139">這是第2版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-140">**cbCoNtextInfo**</span><span class="sxs-lookup"><span data-stu-id="f5d27-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-141">**DWORD** 值，指出 **pbCoNtextInfo** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="f5d27-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="f5d27-142">這是第2版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="f5d27-143">**pszProvName**</span><span class="sxs-lookup"><span data-stu-id="f5d27-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="f5d27-144">字串，其中包含提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5d27-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="f5d27-145">這是第3版的成員。</span><span class="sxs-lookup"><span data-stu-id="f5d27-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5d27-146">備註</span><span class="sxs-lookup"><span data-stu-id="f5d27-146">Remarks</span></span>

<span data-ttu-id="f5d27-147">**VTableProvStruc** 結構中的指標只能在 [**CPAcquireCoNtext**](https://www.bing.com/search?q=**CPAcquireContext**)函數中使用。</span><span class="sxs-lookup"><span data-stu-id="f5d27-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="f5d27-148">如果在呼叫 **CPAcquireCoNtext** 完成後需要結構的成員，則 CSP 必須建立所需結構元素的複本。</span><span class="sxs-lookup"><span data-stu-id="f5d27-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="f5d27-149">您可以儲存和使用此結構中的函式指標，直到發行 CSP 內容為止。</span><span class="sxs-lookup"><span data-stu-id="f5d27-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d27-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5d27-150">Requirements</span></span>



| <span data-ttu-id="f5d27-151">需求</span><span class="sxs-lookup"><span data-stu-id="f5d27-151">Requirement</span></span> | <span data-ttu-id="f5d27-152">值</span><span class="sxs-lookup"><span data-stu-id="f5d27-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d27-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5d27-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d27-154">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5d27-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5d27-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5d27-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d27-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5d27-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5d27-157">標頭</span><span class="sxs-lookup"><span data-stu-id="f5d27-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d27-158"><dt>Cspdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d27-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="f5d27-159">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f5d27-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f5d27-160">**VTableProvStrucW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="f5d27-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
