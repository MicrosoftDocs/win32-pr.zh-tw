---
description: 顯示對應于目前 UI 語言設定的說明視窗。
title: MLHtmlHelp 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841209"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="984e6-103">MLHtmlHelp 函式</span><span class="sxs-lookup"><span data-stu-id="984e6-103">MLHtmlHelp function</span></span>

<span data-ttu-id="984e6-104">\[這項功能可透過 Windows XP 和 Windows Server 2003 取得。</span><span class="sxs-lookup"><span data-stu-id="984e6-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="984e6-105">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="984e6-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="984e6-106">顯示對應于目前 UI 語言設定的說明視窗。</span><span class="sxs-lookup"><span data-stu-id="984e6-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="984e6-107">語法</span><span class="sxs-lookup"><span data-stu-id="984e6-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="984e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="984e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="984e6-109">*hwndCaller* \[在\]</span><span class="sxs-lookup"><span data-stu-id="984e6-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984e6-110">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="984e6-110">Type: **HWND**</span></span>

<span data-ttu-id="984e6-111">呼叫此函式之父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="984e6-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="984e6-112">*pszFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="984e6-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984e6-113">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="984e6-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="984e6-114">緩衝區的指標，其中包含已編譯說明 ( .chm) 檔案的完整路徑，或指定說明檔中的主題檔案。</span><span class="sxs-lookup"><span data-stu-id="984e6-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="984e6-115">*uCommand* \[在\]</span><span class="sxs-lookup"><span data-stu-id="984e6-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984e6-116">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="984e6-116">Type: **UINT**</span></span>

<span data-ttu-id="984e6-117">要完成的命令。</span><span class="sxs-lookup"><span data-stu-id="984e6-117">The command to complete.</span></span> <span data-ttu-id="984e6-118">此函式只會直接支援 [hh \_ 顯示 \_ 主題](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) 和 [hh \_ 顯示 \_ 文字 \_ 快顯視窗](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command)。</span><span class="sxs-lookup"><span data-stu-id="984e6-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="984e6-119">在任何其他命令的情況下，會將不含 *dwCrossCodePage* 值的呼叫轉送至 [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)。</span><span class="sxs-lookup"><span data-stu-id="984e6-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="984e6-120">*dwData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="984e6-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984e6-121">類型： **DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="984e6-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="984e6-122">任何可能需要的資料（根據 *uCommand* 參數的值）。</span><span class="sxs-lookup"><span data-stu-id="984e6-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="984e6-123">*dwCrossCodePage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="984e6-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984e6-124">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="984e6-124">Type: **DWORD**</span></span>

<span data-ttu-id="984e6-125">**DWORD** 值，指出目前 UI 語言設定的字碼頁，例如 CP \_ ACP。</span><span class="sxs-lookup"><span data-stu-id="984e6-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="984e6-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="984e6-126">Return value</span></span>

<span data-ttu-id="984e6-127">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="984e6-127">Type: **HWND**</span></span>

<span data-ttu-id="984e6-128">根據指定的 *uCommand* 和結果， **MLHtmlHelp** 會傳回下列其中一項或兩項：</span><span class="sxs-lookup"><span data-stu-id="984e6-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="984e6-129">說明視窗 (hwnd) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="984e6-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="984e6-130">**Null**。</span><span class="sxs-lookup"><span data-stu-id="984e6-130">**NULL**.</span></span> <span data-ttu-id="984e6-131">在某些情況下， **Null** 表示失敗;在其他情況下， **Null** 表示尚未建立說明視窗。</span><span class="sxs-lookup"><span data-stu-id="984e6-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="984e6-132">備註</span><span class="sxs-lookup"><span data-stu-id="984e6-132">Remarks</span></span>

<span data-ttu-id="984e6-133">如果目前語言的說明檔路徑發生問題，則會將呼叫轉送至 [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) 以進行標準處理。</span><span class="sxs-lookup"><span data-stu-id="984e6-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="984e6-134">當 [說明] 視窗關閉時，除非擁有者為桌面，否則焦點會回到擁有者。</span><span class="sxs-lookup"><span data-stu-id="984e6-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="984e6-135">如果 *hwndCaller* 是桌面，則作業系統會決定傳回焦點的位置。</span><span class="sxs-lookup"><span data-stu-id="984e6-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="984e6-136">此外，如果 **MLHtmlHelp** 從 [說明] 視窗傳送任何通知訊息，只要您已在 [說明] 視窗定義中啟用 [通知訊息](/previous-versions/windows/desktop/htmlhelp/about-notification-messages)追蹤，訊息就會傳送至 *hwndCaller* 。</span><span class="sxs-lookup"><span data-stu-id="984e6-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="984e6-137">範例</span><span class="sxs-lookup"><span data-stu-id="984e6-137">Examples</span></span>

<span data-ttu-id="984e6-138">下列範例會呼叫 [HH \_ DISPLAY \_ 主題](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) 命令以開啟名為 help 的說明檔，並在名為的 [說明] 視窗中顯示其預設主題 `Mainwin` 。</span><span class="sxs-lookup"><span data-stu-id="984e6-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="984e6-139">一般而言，此命令中指定的 [說明] 視窗是標準的 [HTML 說明檢視器](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)。</span><span class="sxs-lookup"><span data-stu-id="984e6-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="984e6-140">使用此函式時，請將裝載可執行檔的堆疊大小設定為至少100k。</span><span class="sxs-lookup"><span data-stu-id="984e6-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="984e6-141">如果定義的堆疊大小太小，則建立來執行 HTML 說明的執行緒也會以這個堆疊大小建立，而作業可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="984e6-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="984e6-142">（選擇性）您可以從 link 命令列中移除/STACK，也可以移除可執行檔 .DEF 檔中的任何堆疊設定 (預設堆疊大小在此案例中為 1MB) 。</span><span class="sxs-lookup"><span data-stu-id="984e6-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="984e6-143">您也可以使用/Fnumber 編譯器命令設定堆疊大小 (編譯器會將此值以/STACK) 的形式傳遞至連結器。</span><span class="sxs-lookup"><span data-stu-id="984e6-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="984e6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="984e6-144">Requirements</span></span>



| <span data-ttu-id="984e6-145">需求</span><span class="sxs-lookup"><span data-stu-id="984e6-145">Requirement</span></span> | <span data-ttu-id="984e6-146">值</span><span class="sxs-lookup"><span data-stu-id="984e6-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984e6-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="984e6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="984e6-148">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="984e6-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="984e6-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="984e6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="984e6-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="984e6-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="984e6-151">標頭</span><span class="sxs-lookup"><span data-stu-id="984e6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="984e6-152"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="984e6-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="984e6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="984e6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="984e6-154"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="984e6-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="984e6-155">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="984e6-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="984e6-156">**MLHtmlHelpW** (Unicode) 和 **MLHtmlHelpA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="984e6-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
