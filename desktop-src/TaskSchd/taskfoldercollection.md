---
title: TaskFolderCollection 物件
description: 編寫物件的腳本物件，該物件會提供包含工作之資料夾集合的資訊和控制權。
ms.assetid: 773d1c86-a539-478d-9e71-dc5b86c098c1
keywords:
- TaskFolderCollection 物件工作排程器
- TaskFolderCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskFolderCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c861322d6868ca7ec9ef861e2c3ea30f624db8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966334"
---
# <a name="taskfoldercollection-object"></a><span data-ttu-id="23720-105">TaskFolderCollection 物件</span><span class="sxs-lookup"><span data-stu-id="23720-105">TaskFolderCollection object</span></span>

<span data-ttu-id="23720-106">編寫物件的腳本物件，該物件會提供包含工作之資料夾集合的資訊和控制權。</span><span class="sxs-lookup"><span data-stu-id="23720-106">Scripting object that provides information and control for a collection of folders that contain tasks.</span></span>

## <a name="members"></a><span data-ttu-id="23720-107">成員</span><span class="sxs-lookup"><span data-stu-id="23720-107">Members</span></span>

<span data-ttu-id="23720-108">**TaskFolderCollection** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="23720-108">The **TaskFolderCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="23720-109">屬性</span><span class="sxs-lookup"><span data-stu-id="23720-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23720-110">屬性</span><span class="sxs-lookup"><span data-stu-id="23720-110">Properties</span></span>

<span data-ttu-id="23720-111">**TaskFolderCollection** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="23720-111">The **TaskFolderCollection** object has these properties.</span></span>



| <span data-ttu-id="23720-112">屬性</span><span class="sxs-lookup"><span data-stu-id="23720-112">Property</span></span>                                               | <span data-ttu-id="23720-113">描述</span><span class="sxs-lookup"><span data-stu-id="23720-113">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="23720-114">**計數**</span><span class="sxs-lookup"><span data-stu-id="23720-114">**Count**</span></span>](taskfoldercollection-count.md)<br/> | <span data-ttu-id="23720-115">取得集合中的資料夾數目。</span><span class="sxs-lookup"><span data-stu-id="23720-115">Gets the number of folders in the collection.</span></span><br/>   |
| [<span data-ttu-id="23720-116">**項目**</span><span class="sxs-lookup"><span data-stu-id="23720-116">**Item**</span></span>](taskfoldercollection-item.md)<br/>   | <span data-ttu-id="23720-117">從集合中取得指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="23720-117">Gets the specified folder from the collection.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="23720-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="23720-118">Requirements</span></span>



| <span data-ttu-id="23720-119">需求</span><span class="sxs-lookup"><span data-stu-id="23720-119">Requirement</span></span> | <span data-ttu-id="23720-120">值</span><span class="sxs-lookup"><span data-stu-id="23720-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23720-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23720-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23720-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23720-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23720-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23720-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23720-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23720-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23720-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="23720-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="23720-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23720-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23720-127">DLL</span><span class="sxs-lookup"><span data-stu-id="23720-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23720-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23720-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23720-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23720-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23720-130">**TaskFolder.GetFolders**</span><span class="sxs-lookup"><span data-stu-id="23720-130">**TaskFolder.GetFolders**</span></span>](taskfolder-getfolders.md)
</dt> </dl>

 

 





