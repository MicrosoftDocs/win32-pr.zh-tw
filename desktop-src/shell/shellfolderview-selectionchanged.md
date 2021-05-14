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
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842569"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="95c4a-103">ShellFolderView. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="95c4a-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="95c4a-104">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="95c4a-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c4a-105">語法</span><span class="sxs-lookup"><span data-stu-id="95c4a-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="95c4a-106">參數</span><span class="sxs-lookup"><span data-stu-id="95c4a-106">Parameters</span></span>

<span data-ttu-id="95c4a-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="95c4a-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c4a-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="95c4a-108">Requirements</span></span>



| <span data-ttu-id="95c4a-109">需求</span><span class="sxs-lookup"><span data-stu-id="95c4a-109">Requirement</span></span> | <span data-ttu-id="95c4a-110">值</span><span class="sxs-lookup"><span data-stu-id="95c4a-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c4a-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95c4a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="95c4a-112">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95c4a-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95c4a-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95c4a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="95c4a-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95c4a-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95c4a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="95c4a-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c4a-116"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="95c4a-117">Idl</span><span class="sxs-lookup"><span data-stu-id="95c4a-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95c4a-118"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="95c4a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="95c4a-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95c4a-120"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="95c4a-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




