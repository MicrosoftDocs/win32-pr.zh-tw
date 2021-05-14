---
description: 指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。
title: 'FMExtensionProc 回呼函數 (Wfext) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842239"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="724c6-103">FMExtensionProc 回呼函式</span><span class="sxs-lookup"><span data-stu-id="724c6-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="724c6-104">指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。</span><span class="sxs-lookup"><span data-stu-id="724c6-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="724c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="724c6-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="724c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="724c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724c6-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="724c6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="724c6-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="724c6-108">Type: **HWND**</span></span>

<span data-ttu-id="724c6-109">檔案管理員的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="724c6-109">A window handle to File Manager.</span></span> <span data-ttu-id="724c6-110">延伸模組會使用此控制碼來指定它必須顯示之任何對話方塊或訊息方塊的父視窗，以及將查詢訊息傳送至 [檔案管理員]。</span><span class="sxs-lookup"><span data-stu-id="724c6-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="724c6-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="724c6-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="724c6-112">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="724c6-112">Type: **WORD**</span></span>

<span data-ttu-id="724c6-113">下列其中一個檔案管理員訊息。</span><span class="sxs-lookup"><span data-stu-id="724c6-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="724c6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1至99**</span><span class="sxs-lookup"><span data-stu-id="724c6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-115">使用者從擴充功能提供的功能表中選取專案。</span><span class="sxs-lookup"><span data-stu-id="724c6-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="724c6-116">值是選取之功能表項目的識別碼。</span><span class="sxs-lookup"><span data-stu-id="724c6-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="724c6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="724c6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-118">在選取擴充功能功能表或工具列命令專案時，使用者按下 F1。</span><span class="sxs-lookup"><span data-stu-id="724c6-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="724c6-119">指出延伸模組應針對命令專案適當地呼叫 **WinHelp** 。</span><span class="sxs-lookup"><span data-stu-id="724c6-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="724c6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="724c6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-121">使用者選取了延伸功能表或工具列命令專案。</span><span class="sxs-lookup"><span data-stu-id="724c6-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="724c6-122">指出延伸模組應提供說明字串。</span><span class="sxs-lookup"><span data-stu-id="724c6-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="724c6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="724c6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-124">使用者選取了擴充功能的功能表。</span><span class="sxs-lookup"><span data-stu-id="724c6-124">User selected the extension's menu.</span></span> <span data-ttu-id="724c6-125">擴充功能應該將功能表中的專案初始化。</span><span class="sxs-lookup"><span data-stu-id="724c6-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="724c6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ 載入**</span><span class="sxs-lookup"><span data-stu-id="724c6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-127">檔案管理員正在載入延伸模組 DLL，並提示 DLL 提供 DLL 提供之功能表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="724c6-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="724c6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="724c6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-129">[ **檔案管理員** 目錄] 視窗或 [ **搜尋結果** ] 視窗中的選取專案已變更。</span><span class="sxs-lookup"><span data-stu-id="724c6-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="724c6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="724c6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-131">[檔案管理員] 正在建立工具列，並提示副檔名 DLL 提供 DLL 加入工具列之任何按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="724c6-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="724c6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**</span><span class="sxs-lookup"><span data-stu-id="724c6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-133">檔案管理員正在卸載擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="724c6-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="724c6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT \_ 使用者重新整理 \_**</span><span class="sxs-lookup"><span data-stu-id="724c6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="724c6-135">使用者已從 **[** **視窗]** 功能表中選取 [重新整理] 命令。</span><span class="sxs-lookup"><span data-stu-id="724c6-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="724c6-136">必要時，擴充功能應該更新功能表中的專案。</span><span class="sxs-lookup"><span data-stu-id="724c6-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="724c6-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="724c6-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="724c6-138">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="724c6-138">Type: **LONG**</span></span>

<span data-ttu-id="724c6-139">訊息特定的值。</span><span class="sxs-lookup"><span data-stu-id="724c6-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724c6-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="724c6-140">Return value</span></span>

<span data-ttu-id="724c6-141">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="724c6-141">Type: **LONG**</span></span>

<span data-ttu-id="724c6-142">傳回相依于 *wMsg* 參數訊息的值。</span><span class="sxs-lookup"><span data-stu-id="724c6-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="724c6-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="724c6-143">Requirements</span></span>



| <span data-ttu-id="724c6-144">需求</span><span class="sxs-lookup"><span data-stu-id="724c6-144">Requirement</span></span> | <span data-ttu-id="724c6-145">值</span><span class="sxs-lookup"><span data-stu-id="724c6-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="724c6-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="724c6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="724c6-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="724c6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="724c6-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="724c6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="724c6-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="724c6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="724c6-150">標頭</span><span class="sxs-lookup"><span data-stu-id="724c6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="724c6-151"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="724c6-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="724c6-152">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="724c6-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="724c6-153">**FMExtensionProcW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="724c6-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




