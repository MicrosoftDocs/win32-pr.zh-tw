---
description: 搭配 Rundll32.exe 使用時，會啟動 Passport Wizard。
title: PassportWizardRunDll 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842509"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="c6e0b-103">PassportWizardRunDll 函式</span><span class="sxs-lookup"><span data-stu-id="c6e0b-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="c6e0b-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c6e0b-105">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c6e0b-106">搭配 Rundll32.exe 使用時，會啟動 Passport Wizard。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e0b-107">語法</span><span class="sxs-lookup"><span data-stu-id="c6e0b-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="c6e0b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c6e0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e0b-109">*hwndStub* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e0b-110">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="c6e0b-110">Type: **HWND**</span></span>

<span data-ttu-id="c6e0b-111">主控視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-111">A handle to an owner window.</span></span> <span data-ttu-id="c6e0b-112">此參數通常會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c6e0b-113">*hAppInstance* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e0b-114">類型： **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="c6e0b-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="c6e0b-115">程式庫檔案的控制碼，以 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ( "netplwiz" ) 的傳回值形式取得。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="c6e0b-116">*lpszCmdLine* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e0b-117">類型： **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="c6e0b-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="c6e0b-118">引數資料。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-118">Argument data.</span></span> <span data-ttu-id="c6e0b-119">這個值一律是空的。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="c6e0b-120">*nCmdShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e0b-121">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="c6e0b-121">Type: **int**</span></span>

<span data-ttu-id="c6e0b-122">設定視窗的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e0b-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6e0b-123">Return value</span></span>

<span data-ttu-id="c6e0b-124">無。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e0b-125">備註</span><span class="sxs-lookup"><span data-stu-id="c6e0b-125">Remarks</span></span>

<span data-ttu-id="c6e0b-126">Passport Wizard 可用來取得 Windows 的預設 Passport。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="c6e0b-127">Passport 可讓使用者使用使用者的電子郵件地址，個人化存取所有的 MSN 網站和其他具備 Passport 功能的網站。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="c6e0b-128">透過 Rundll32.exe 命令使用 **PassportWizardRunDll** 做為 Netplwiz.dll 檔案的進入點，可讓您從命令列啟動 Passport Wizard，就好像它是可執行檔一樣。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="c6e0b-129">**PassportWizardRunDll** 只會在 Rundll32.exe 命令的內容中使用，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c6e0b-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="c6e0b-130">**rundll32.exe netplwiz.dll、PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="c6e0b-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="c6e0b-131">使用進入點函式搭配 Rundll32.exe 不像一般函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="c6e0b-132">函式名稱和儲存的 .dll 檔案的名稱只會用來做為命令列參數。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="c6e0b-133">在 [語法] 下顯示的函式定義，只是您可以使用 Rundll32.exe 呼叫的所有函式的標準原型。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="c6e0b-134">*HwndStub*、 *hAppInstance* 和 *nCmdShow* 的特定值不是由使用者提供，而是由 rundll32.exe 在幕後處理。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="c6e0b-135">**PassportWizardRunDll** 不會使用 *lpszCmdLine* 值，因此不需要額外的資料。</span><span class="sxs-lookup"><span data-stu-id="c6e0b-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e0b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6e0b-136">Requirements</span></span>



| <span data-ttu-id="c6e0b-137">需求</span><span class="sxs-lookup"><span data-stu-id="c6e0b-137">Requirement</span></span> | <span data-ttu-id="c6e0b-138">值</span><span class="sxs-lookup"><span data-stu-id="c6e0b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e0b-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6e0b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e0b-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="c6e0b-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6e0b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e0b-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6e0b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c6e0b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="c6e0b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e0b-144"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="c6e0b-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="c6e0b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e0b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e0b-146"><dt>Netplwiz.dll (5.60 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c6e0b-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
