---
description: 本節說明 Windows Shell 回呼函數。
title: Shell 回呼函數
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386120"
---
# <a name="shell-callback-functions"></a><span data-ttu-id="eb831-103">Shell 回呼函數</span><span class="sxs-lookup"><span data-stu-id="eb831-103">Shell Callback Functions</span></span>

<span data-ttu-id="eb831-104">本節說明 Windows Shell 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="eb831-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb831-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="eb831-105">In this section</span></span>



| <span data-ttu-id="eb831-106">主題</span><span class="sxs-lookup"><span data-stu-id="eb831-106">Topic</span></span>                                                                     | <span data-ttu-id="eb831-107">描述</span><span class="sxs-lookup"><span data-stu-id="eb831-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb831-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb831-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="eb831-109">指定應用程式定義的回呼函式，這個函式用來傳送訊息，以及處理來自的訊息，以回應 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)的呼叫所顯示的 **流覽** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eb831-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="eb831-110">*FMExtensionProc*</span><span class="sxs-lookup"><span data-stu-id="eb831-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="eb831-111">指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。</span><span class="sxs-lookup"><span data-stu-id="eb831-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb831-112">*MRUCMPPROC*</span><span class="sxs-lookup"><span data-stu-id="eb831-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="eb831-113">用來判斷專案是否存在於最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="eb831-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="eb831-114">**PAPPSTATE \_ 變更 \_ 常式**</span><span class="sxs-lookup"><span data-stu-id="eb831-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="eb831-115">指定應用程式定義的回呼函式，此函式會在應用程式進入或離開暫停狀態時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb831-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb831-116">**SUBCLASSPROC**</span><span class="sxs-lookup"><span data-stu-id="eb831-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="eb831-117">定義 [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) 和 [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)所使用之回呼函式的原型。</span><span class="sxs-lookup"><span data-stu-id="eb831-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="eb831-118">**FM 取消 \_ 刪除 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="eb831-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="eb831-119">當使用者選擇 [檔案] 功能表中的 [取消 **刪除** ] 命令時，指定 **由 [檔** 管理器] 呼叫的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="eb831-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
