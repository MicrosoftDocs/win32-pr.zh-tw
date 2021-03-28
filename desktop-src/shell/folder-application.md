---
description: 包含資料夾的應用程式物件。
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: '資料夾。應用程式屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468605"
---
# <a name="folderapplication-property"></a><span data-ttu-id="d212d-103">資料夾。應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="d212d-103">Folder.Application property</span></span>

<span data-ttu-id="d212d-104">包含資料夾的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="d212d-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="d212d-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d212d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d212d-106">語法</span><span class="sxs-lookup"><span data-stu-id="d212d-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="d212d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="d212d-107">Property value</span></span>

<span data-ttu-id="d212d-108">應用程式物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="d212d-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d212d-109">備註</span><span class="sxs-lookup"><span data-stu-id="d212d-109">Remarks</span></span>

<span data-ttu-id="d212d-110">如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="d212d-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="d212d-111">否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。</span><span class="sxs-lookup"><span data-stu-id="d212d-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="d212d-112">使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Internet Explorer 應用程式的實例。</span><span class="sxs-lookup"><span data-stu-id="d212d-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="d212d-113">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="d212d-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="d212d-114">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="d212d-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="d212d-115">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d212d-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d212d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d212d-116">Requirements</span></span>



| <span data-ttu-id="d212d-117">需求</span><span class="sxs-lookup"><span data-stu-id="d212d-117">Requirement</span></span> | <span data-ttu-id="d212d-118">值</span><span class="sxs-lookup"><span data-stu-id="d212d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d212d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d212d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d212d-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d212d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="d212d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d212d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d212d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d212d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d212d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d212d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d212d-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d212d-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d212d-125">Idl</span><span class="sxs-lookup"><span data-stu-id="d212d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d212d-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d212d-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




