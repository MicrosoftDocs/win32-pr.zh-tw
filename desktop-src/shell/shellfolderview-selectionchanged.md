---
description: 發生于視圖中任何專案或專案的選取狀態變更時。
title: 'ShellFolderView. SelectionChanged 事件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: 864cd4c7bb0b414e4237c698412ad10899c8cbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027336"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="c4833-103">ShellFolderView. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="c4833-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="c4833-104">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="c4833-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4833-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4833-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="c4833-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4833-106">Parameters</span></span>

<span data-ttu-id="c4833-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="c4833-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4833-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4833-108">Requirements</span></span>



| <span data-ttu-id="c4833-109">需求</span><span class="sxs-lookup"><span data-stu-id="c4833-109">Requirement</span></span> | <span data-ttu-id="c4833-110">值</span><span class="sxs-lookup"><span data-stu-id="c4833-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4833-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4833-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c4833-112">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4833-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4833-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4833-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c4833-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4833-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4833-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c4833-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4833-116"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4833-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c4833-117">Idl</span><span class="sxs-lookup"><span data-stu-id="c4833-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4833-118"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4833-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c4833-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c4833-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4833-120"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c4833-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




