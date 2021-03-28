---
description: 包含資料夾專案集合的應用程式物件。
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: 'FolderItems： Application 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111724"
---
# <a name="folderitemsapplication-property"></a><span data-ttu-id="407a6-103">FolderItems。應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="407a6-103">FolderItems.Application property</span></span>

<span data-ttu-id="407a6-104">包含資料夾專案集合的 **應用程式** 物件。</span><span class="sxs-lookup"><span data-stu-id="407a6-104">Contains the **Application** object of the folder items collection.</span></span>

<span data-ttu-id="407a6-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="407a6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="407a6-106">語法</span><span class="sxs-lookup"><span data-stu-id="407a6-106">Syntax</span></span>


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a><span data-ttu-id="407a6-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="407a6-107">Property value</span></span>

<span data-ttu-id="407a6-108">應用程式物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="407a6-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="407a6-109">備註</span><span class="sxs-lookup"><span data-stu-id="407a6-109">Remarks</span></span>

<span data-ttu-id="407a6-110">如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="407a6-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="407a6-111">否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="407a6-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="407a6-112">使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Windows Internet Explorer 應用程式的實例。</span><span class="sxs-lookup"><span data-stu-id="407a6-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="407a6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="407a6-113">Requirements</span></span>



| <span data-ttu-id="407a6-114">需求</span><span class="sxs-lookup"><span data-stu-id="407a6-114">Requirement</span></span> | <span data-ttu-id="407a6-115">值</span><span class="sxs-lookup"><span data-stu-id="407a6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="407a6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="407a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="407a6-117">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="407a6-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="407a6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="407a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="407a6-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="407a6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="407a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="407a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="407a6-121"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="407a6-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="407a6-122">Idl</span><span class="sxs-lookup"><span data-stu-id="407a6-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="407a6-123"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="407a6-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="407a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="407a6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="407a6-125"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="407a6-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




