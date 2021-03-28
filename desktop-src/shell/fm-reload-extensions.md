---
description: 由檔案管理員延伸模組 (或其他應用程式所傳送) ，使檔案管理員重載 Winfile.ini 檔的附加元件區段中所列的所有擴充 Dll \[ \] 。
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: 'FM_RELOAD_EXTENSIONS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973229"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="70d64-103">FM \_ 重載 \_ 延伸模組訊息</span><span class="sxs-lookup"><span data-stu-id="70d64-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="70d64-104">由檔案管理員延伸模組 (或其他應用程式所傳送) ，使檔案管理員重載 Winfile.ini 檔的附加元件區段中所列的所有擴充 Dll \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="70d64-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="70d64-105">參數</span><span class="sxs-lookup"><span data-stu-id="70d64-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d64-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70d64-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70d64-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="70d64-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="70d64-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70d64-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70d64-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="70d64-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d64-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="70d64-110">Return value</span></span>

<span data-ttu-id="70d64-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="70d64-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70d64-112">備註</span><span class="sxs-lookup"><span data-stu-id="70d64-112">Remarks</span></span>

<span data-ttu-id="70d64-113">其他應用程式可以使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式將此訊息傳送至檔案管理員。</span><span class="sxs-lookup"><span data-stu-id="70d64-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="70d64-114">若要取得適當的檔案管理員視窗控制碼，應用程式可以在 FindWindow 函式的呼叫中指定 "WFS \_ Frame [](/windows/win32/api/winuser/nf-winuser-findwindowa) " 作為 *lpszClassName* 參數。</span><span class="sxs-lookup"><span data-stu-id="70d64-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70d64-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="70d64-115">Requirements</span></span>



| <span data-ttu-id="70d64-116">需求</span><span class="sxs-lookup"><span data-stu-id="70d64-116">Requirement</span></span> | <span data-ttu-id="70d64-117">值</span><span class="sxs-lookup"><span data-stu-id="70d64-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70d64-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70d64-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70d64-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70d64-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="70d64-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70d64-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70d64-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70d64-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70d64-122">標頭</span><span class="sxs-lookup"><span data-stu-id="70d64-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70d64-123"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="70d64-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d64-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70d64-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d64-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="70d64-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
