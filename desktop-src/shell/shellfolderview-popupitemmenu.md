---
description: ShellFolderView. PopupItemMenu 方法-為指定的專案建立快捷方式功能表，並傳回選取的命令字串。
title: 'ShellFolderView. PopupItemMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083386"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="f3346-103">ShellFolderView. PopupItemMenu 方法</span><span class="sxs-lookup"><span data-stu-id="f3346-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="f3346-104">為指定的專案建立快捷方式功能表，並傳回選取的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f3346-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3346-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3346-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="f3346-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3346-107">*vItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3346-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3346-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="f3346-108">Type: **Variant**</span></span>

<span data-ttu-id="f3346-109">將建立快捷方式功能表的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f3346-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="f3346-110">*vx* \[ in、optional\]</span><span class="sxs-lookup"><span data-stu-id="f3346-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3346-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="f3346-111">Type: **Variant**</span></span>

<span data-ttu-id="f3346-112">功能表的水準位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3346-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f3346-113">*vy* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f3346-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3346-114">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="f3346-114">Type: **Variant**</span></span>

<span data-ttu-id="f3346-115">功能表的垂直位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3346-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3346-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3346-116">Return value</span></span>

<span data-ttu-id="f3346-117">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="f3346-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="f3346-118">接收命令字串的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="f3346-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3346-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3346-119">Requirements</span></span>



| <span data-ttu-id="f3346-120">需求</span><span class="sxs-lookup"><span data-stu-id="f3346-120">Requirement</span></span> | <span data-ttu-id="f3346-121">值</span><span class="sxs-lookup"><span data-stu-id="f3346-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3346-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3346-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3346-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3346-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3346-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3346-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3346-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3346-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f3346-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f3346-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3346-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3346-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f3346-128">Idl</span><span class="sxs-lookup"><span data-stu-id="f3346-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3346-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3346-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f3346-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f3346-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3346-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f3346-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
