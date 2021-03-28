---
description: 表示屬於 Shell 之開啟視窗的集合。 與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: 'ShellWindows 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973277"
---
# <a name="shellwindows-object"></a><span data-ttu-id="7f4dd-104">ShellWindows 物件</span><span class="sxs-lookup"><span data-stu-id="7f4dd-104">ShellWindows object</span></span>

<span data-ttu-id="7f4dd-105">表示屬於 Shell 之開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="7f4dd-106">與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="7f4dd-107">成員</span><span class="sxs-lookup"><span data-stu-id="7f4dd-107">Members</span></span>

<span data-ttu-id="7f4dd-108">**ShellWindows** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f4dd-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="7f4dd-109">方法</span><span class="sxs-lookup"><span data-stu-id="7f4dd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f4dd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7f4dd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f4dd-111">方法</span><span class="sxs-lookup"><span data-stu-id="7f4dd-111">Methods</span></span>

<span data-ttu-id="7f4dd-112">**ShellWindows** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="7f4dd-113">方法</span><span class="sxs-lookup"><span data-stu-id="7f4dd-113">Method</span></span>                                                 | <span data-ttu-id="7f4dd-114">描述</span><span class="sxs-lookup"><span data-stu-id="7f4dd-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f4dd-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="7f4dd-116">建立並傳回新的 **ShellWindows** 物件，該物件為這個 **ShellWindows** 物件的複本。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="7f4dd-117">**項目**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="7f4dd-118">捕獲代表 Shell 視窗的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f4dd-119">屬性</span><span class="sxs-lookup"><span data-stu-id="7f4dd-119">Properties</span></span>

<span data-ttu-id="7f4dd-120">**ShellWindows** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="7f4dd-121">屬性</span><span class="sxs-lookup"><span data-stu-id="7f4dd-121">Property</span></span>                                       | <span data-ttu-id="7f4dd-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="7f4dd-122">Access type</span></span>          | <span data-ttu-id="7f4dd-123">Description</span><span class="sxs-lookup"><span data-stu-id="7f4dd-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="7f4dd-124">**計數**</span><span class="sxs-lookup"><span data-stu-id="7f4dd-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="7f4dd-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f4dd-125">Read-only</span></span><br/> | <span data-ttu-id="7f4dd-126">包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="7f4dd-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f4dd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f4dd-127">Requirements</span></span>



| <span data-ttu-id="7f4dd-128">需求</span><span class="sxs-lookup"><span data-stu-id="7f4dd-128">Requirement</span></span> | <span data-ttu-id="7f4dd-129">值</span><span class="sxs-lookup"><span data-stu-id="7f4dd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4dd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f4dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4dd-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f4dd-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f4dd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f4dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4dd-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f4dd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f4dd-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7f4dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4dd-135"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f4dd-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="7f4dd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7f4dd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f4dd-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7f4dd-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
