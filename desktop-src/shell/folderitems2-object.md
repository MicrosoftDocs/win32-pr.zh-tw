---
description: 擴充 FolderItems 物件。 它支援一個額外的方法。
title: 'FolderItems2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0ca0efb3-6831-4561-9fd1-6d0b62704931
ms.openlocfilehash: b11bc4d1b3cd2bdd71802e79ca959c0a0f84e360
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840969"
---
# <a name="folderitems2-object"></a><span data-ttu-id="79722-104">FolderItems2 物件</span><span class="sxs-lookup"><span data-stu-id="79722-104">FolderItems2 object</span></span>

<span data-ttu-id="79722-105">擴充 [**FolderItems**](folderitems.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="79722-105">Extends the [**FolderItems**](folderitems.md) object.</span></span> <span data-ttu-id="79722-106">它支援一個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="79722-106">It supports one additional method.</span></span>

## <a name="members"></a><span data-ttu-id="79722-107">成員</span><span class="sxs-lookup"><span data-stu-id="79722-107">Members</span></span>

<span data-ttu-id="79722-108">**FolderItems2** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="79722-108">The **FolderItems2** object has these types of members:</span></span>

-   [<span data-ttu-id="79722-109">方法</span><span class="sxs-lookup"><span data-stu-id="79722-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79722-110">方法</span><span class="sxs-lookup"><span data-stu-id="79722-110">Methods</span></span>

<span data-ttu-id="79722-111">**FolderItems2** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="79722-111">The **FolderItems2** object has these methods.</span></span>



| <span data-ttu-id="79722-112">方法</span><span class="sxs-lookup"><span data-stu-id="79722-112">Method</span></span>                                            | <span data-ttu-id="79722-113">描述</span><span class="sxs-lookup"><span data-stu-id="79722-113">Description</span></span>                                                                                                                                                                                                                                         |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79722-114">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="79722-114">**InvokeVerbEx**</span></span>](folderitems2-invokeverbex.md) | <span data-ttu-id="79722-115">在 [**FolderItem**](folderitem.md) 物件的集合上執行動詞。</span><span class="sxs-lookup"><span data-stu-id="79722-115">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="79722-116">這個方法是 [**InvokeVerb**](folderitem-invokeverb.md) 方法的擴充功能，可讓您透過一組旗標來進行作業的額外控制。</span><span class="sxs-lookup"><span data-stu-id="79722-116">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79722-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="79722-117">Requirements</span></span>



| <span data-ttu-id="79722-118">需求</span><span class="sxs-lookup"><span data-stu-id="79722-118">Requirement</span></span> | <span data-ttu-id="79722-119">值</span><span class="sxs-lookup"><span data-stu-id="79722-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79722-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79722-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79722-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79722-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79722-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79722-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79722-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79722-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="79722-124">標頭</span><span class="sxs-lookup"><span data-stu-id="79722-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79722-125"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="79722-125"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="79722-126">Idl</span><span class="sxs-lookup"><span data-stu-id="79722-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79722-127"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="79722-127"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="79722-128">DLL</span><span class="sxs-lookup"><span data-stu-id="79722-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79722-129"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="79722-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79722-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79722-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79722-131">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="79722-131">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="79722-132">**ShellExecuteEx**</span><span class="sxs-lookup"><span data-stu-id="79722-132">**ShellExecuteEx**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)
</dt> </dl>

 

 




