---
title: 將 ADSI Visual Basic 程式碼對應至 c + + 程式碼
description: ADSI 包含50以上的介面。
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965152"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="b8e47-103">將 ADSI Visual Basic 程式碼對應至 c + + 程式碼</span><span class="sxs-lookup"><span data-stu-id="b8e47-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="b8e47-104">ADSI 包含50以上的介面。</span><span class="sxs-lookup"><span data-stu-id="b8e47-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="b8e47-105">大部分的目錄作業只能使用五個介面完成。</span><span class="sxs-lookup"><span data-stu-id="b8e47-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="b8e47-106">這些包括：</span><span class="sxs-lookup"><span data-stu-id="b8e47-106">They are:</span></span>

-   [<span data-ttu-id="b8e47-107">**IADsOpenDSObject**</span><span class="sxs-lookup"><span data-stu-id="b8e47-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="b8e47-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="b8e47-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="b8e47-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="b8e47-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="b8e47-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="b8e47-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="b8e47-111">**>idirectorysearch**</span><span class="sxs-lookup"><span data-stu-id="b8e47-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="b8e47-112">下表列出從 ADSI VB/VBS 程式碼到 c + + 程式碼的對應。</span><span class="sxs-lookup"><span data-stu-id="b8e47-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="b8e47-113">請注意，這不是完整的清單。</span><span class="sxs-lookup"><span data-stu-id="b8e47-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="b8e47-114">VBS 程式碼</span><span class="sxs-lookup"><span data-stu-id="b8e47-114">VBS Code</span></span>                           | <span data-ttu-id="b8e47-115">VC 程式碼</span><span class="sxs-lookup"><span data-stu-id="b8e47-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b8e47-116">Set obj = GetObject () </span><span class="sxs-lookup"><span data-stu-id="b8e47-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="b8e47-117">hr = AdsGetObject () </span><span class="sxs-lookup"><span data-stu-id="b8e47-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="b8e47-118">Obj。Put obj。取得 obj。父母</span><span class="sxs-lookup"><span data-stu-id="b8e47-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="b8e47-119">IADs 或 IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="b8e47-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="b8e47-120">Obj。建立 obj。刪除 obj。MoveHere</span><span class="sxs-lookup"><span data-stu-id="b8e47-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="b8e47-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="b8e47-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="b8e47-122">針對每個 .。。</span><span class="sxs-lookup"><span data-stu-id="b8e47-122">For each…</span></span> <span data-ttu-id="b8e47-123">在 .。。</span><span class="sxs-lookup"><span data-stu-id="b8e47-123">in…</span></span>                      | <span data-ttu-id="b8e47-124">AdsBuildEnumerator () ADsEnumerateNext () </span><span class="sxs-lookup"><span data-stu-id="b8e47-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="b8e47-125">連接、命令、記錄集</span><span class="sxs-lookup"><span data-stu-id="b8e47-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="b8e47-126">>idirectorysearch</span><span class="sxs-lookup"><span data-stu-id="b8e47-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="b8e47-127">安全描述項、ACL、ACE</span><span class="sxs-lookup"><span data-stu-id="b8e47-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="b8e47-128">IADsSecurityDescriptor、IADsAccessControlList、IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="b8e47-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




