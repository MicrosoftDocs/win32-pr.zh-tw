---
title: 'HWINEVENTHOOK (Windef) '
description: 用來宣告視窗事件攔截函式。
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966313"
---
# <a name="hwineventhook"></a><span data-ttu-id="c15b1-104">HWINEVENTHOOK</span><span class="sxs-lookup"><span data-stu-id="c15b1-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="c15b1-105">用來宣告視窗事件攔截函式。</span><span class="sxs-lookup"><span data-stu-id="c15b1-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="c15b1-106">備註</span><span class="sxs-lookup"><span data-stu-id="c15b1-106">Remarks</span></span>

<span data-ttu-id="c15b1-107">這個資料類型會與 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函式和 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 和 [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c15b1-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15b1-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="c15b1-108">Requirements</span></span>



| <span data-ttu-id="c15b1-109">需求</span><span class="sxs-lookup"><span data-stu-id="c15b1-109">Requirement</span></span> | <span data-ttu-id="c15b1-110">值</span><span class="sxs-lookup"><span data-stu-id="c15b1-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c15b1-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c15b1-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c15b1-112">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c15b1-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c15b1-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c15b1-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c15b1-114">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c15b1-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="c15b1-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c15b1-115">Redistributable</span></span><br/>          | <span data-ttu-id="c15b1-116">使用 SP6 和更新版本和 Windows 95 在 Windows NT 4.0 上 Active Accessibility 1.3 的 RDK</span><span class="sxs-lookup"><span data-stu-id="c15b1-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="c15b1-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c15b1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c15b1-118"><dt>Windef .h (WINVER >= 0x0500)  (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c15b1-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





