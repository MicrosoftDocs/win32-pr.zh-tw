---
description: ShellFolderView：應用程式屬性-包含物件的應用程式物件。
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: 'ShellFolderView： Application 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083466"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="d8692-103">ShellFolderView。應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="d8692-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="d8692-104">包含物件的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="d8692-104">Contains the object's Application object.</span></span>

<span data-ttu-id="d8692-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d8692-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8692-106">語法</span><span class="sxs-lookup"><span data-stu-id="d8692-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="d8692-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8692-107">Property value</span></span>

<span data-ttu-id="d8692-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，會接收應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="d8692-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8692-109">備註</span><span class="sxs-lookup"><span data-stu-id="d8692-109">Remarks</span></span>

<span data-ttu-id="d8692-110">如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="d8692-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="d8692-111">否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="d8692-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="d8692-112">使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Windows Internet Explorer 應用程式的實例。</span><span class="sxs-lookup"><span data-stu-id="d8692-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8692-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8692-113">Requirements</span></span>



| <span data-ttu-id="d8692-114">需求</span><span class="sxs-lookup"><span data-stu-id="d8692-114">Requirement</span></span> | <span data-ttu-id="d8692-115">值</span><span class="sxs-lookup"><span data-stu-id="d8692-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8692-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8692-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8692-117">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8692-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d8692-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8692-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8692-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8692-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8692-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d8692-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8692-121"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8692-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d8692-122">Idl</span><span class="sxs-lookup"><span data-stu-id="d8692-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8692-123"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8692-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d8692-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d8692-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8692-125"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d8692-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
