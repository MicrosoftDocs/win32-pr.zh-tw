---
description: 擴充 FolderItem 物件。 除了 FolderItem 支援的屬性和方法之外，ShellFolderItem 還有兩個額外的方法。
title: 'ShellFolderItem 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973589"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="838ab-104">ShellFolderItem 物件</span><span class="sxs-lookup"><span data-stu-id="838ab-104">ShellFolderItem object</span></span>

<span data-ttu-id="838ab-105">擴充 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="838ab-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="838ab-106">除了 **FolderItem** 支援的屬性和方法之外， **ShellFolderItem** 還有兩個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="838ab-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="838ab-107">成員</span><span class="sxs-lookup"><span data-stu-id="838ab-107">Members</span></span>

<span data-ttu-id="838ab-108">**ShellFolderItem** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="838ab-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="838ab-109">方法</span><span class="sxs-lookup"><span data-stu-id="838ab-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="838ab-110">方法</span><span class="sxs-lookup"><span data-stu-id="838ab-110">Methods</span></span>

<span data-ttu-id="838ab-111">**ShellFolderItem** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="838ab-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="838ab-112">方法</span><span class="sxs-lookup"><span data-stu-id="838ab-112">Method</span></span>                                                       | <span data-ttu-id="838ab-113">描述</span><span class="sxs-lookup"><span data-stu-id="838ab-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="838ab-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="838ab-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="838ab-115">從專案的屬性集取得屬性的值。</span><span class="sxs-lookup"><span data-stu-id="838ab-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="838ab-116">屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。</span><span class="sxs-lookup"><span data-stu-id="838ab-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="838ab-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="838ab-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="838ab-118">在 Shell 專案上執行動詞命令。</span><span class="sxs-lookup"><span data-stu-id="838ab-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="838ab-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="838ab-119">Requirements</span></span>



| <span data-ttu-id="838ab-120">需求</span><span class="sxs-lookup"><span data-stu-id="838ab-120">Requirement</span></span> | <span data-ttu-id="838ab-121">值</span><span class="sxs-lookup"><span data-stu-id="838ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838ab-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="838ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="838ab-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="838ab-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="838ab-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="838ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="838ab-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="838ab-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="838ab-126">標頭</span><span class="sxs-lookup"><span data-stu-id="838ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="838ab-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="838ab-128">Idl</span><span class="sxs-lookup"><span data-stu-id="838ab-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="838ab-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="838ab-130">DLL</span><span class="sxs-lookup"><span data-stu-id="838ab-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="838ab-131"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="838ab-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




