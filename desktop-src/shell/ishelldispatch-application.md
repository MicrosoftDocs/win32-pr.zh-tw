---
description: 包含代表應用程式的物件。
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: 'IShellDispatch： Application 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512232"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="71fd8-103">IShellDispatch。應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="71fd8-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="71fd8-104">包含代表應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="71fd8-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="71fd8-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="71fd8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71fd8-106">語法</span><span class="sxs-lookup"><span data-stu-id="71fd8-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="71fd8-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="71fd8-107">Property value</span></span>

<span data-ttu-id="71fd8-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，會接收應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="71fd8-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="71fd8-109">備註</span><span class="sxs-lookup"><span data-stu-id="71fd8-109">Remarks</span></span>

<span data-ttu-id="71fd8-110">這個屬性是透過 [**EjectPC**](shell-ejectpc.md) 屬性來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="71fd8-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="71fd8-111">如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="71fd8-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="71fd8-112">否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="71fd8-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="71fd8-113">使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Windows Internet Explorer 應用程式的實例。</span><span class="sxs-lookup"><span data-stu-id="71fd8-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="71fd8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="71fd8-114">Requirements</span></span>



| <span data-ttu-id="71fd8-115">需求</span><span class="sxs-lookup"><span data-stu-id="71fd8-115">Requirement</span></span> | <span data-ttu-id="71fd8-116">值</span><span class="sxs-lookup"><span data-stu-id="71fd8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71fd8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71fd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71fd8-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71fd8-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="71fd8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71fd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71fd8-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71fd8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71fd8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="71fd8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71fd8-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="71fd8-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="71fd8-123">Idl</span><span class="sxs-lookup"><span data-stu-id="71fd8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71fd8-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="71fd8-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="71fd8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71fd8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71fd8-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="71fd8-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
