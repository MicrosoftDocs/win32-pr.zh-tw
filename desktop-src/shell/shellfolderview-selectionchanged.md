---
description: ShellFolderView. SelectionChanged 事件-在 view 中的任何專案或專案的選取狀態變更時，就會發生此事件。
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
ms.openlocfilehash: 31a32865a979bf6b5fa115912bdc32a9680e5064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103996"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="41b98-103">ShellFolderView. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="41b98-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="41b98-104">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="41b98-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b98-105">語法</span><span class="sxs-lookup"><span data-stu-id="41b98-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="41b98-106">參數</span><span class="sxs-lookup"><span data-stu-id="41b98-106">Parameters</span></span>

<span data-ttu-id="41b98-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="41b98-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b98-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b98-108">Requirements</span></span>



| <span data-ttu-id="41b98-109">需求</span><span class="sxs-lookup"><span data-stu-id="41b98-109">Requirement</span></span> | <span data-ttu-id="41b98-110">值</span><span class="sxs-lookup"><span data-stu-id="41b98-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b98-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41b98-111">Minimum supported client</span></span><br/> | <span data-ttu-id="41b98-112">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b98-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41b98-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41b98-113">Minimum supported server</span></span><br/> | <span data-ttu-id="41b98-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b98-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41b98-115">標頭</span><span class="sxs-lookup"><span data-stu-id="41b98-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b98-116"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="41b98-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41b98-117">Idl</span><span class="sxs-lookup"><span data-stu-id="41b98-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41b98-118"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="41b98-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41b98-119">DLL</span><span class="sxs-lookup"><span data-stu-id="41b98-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b98-120"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="41b98-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




