---
title: WinNT 的 ADSI 物件
description: ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI、ADSI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092203"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="9255a-104">WinNT 的 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="9255a-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="9255a-105">ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。</span><span class="sxs-lookup"><span data-stu-id="9255a-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9255a-106">ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="9255a-106">ADSI Object</span></span></th>
<th><span data-ttu-id="9255a-107">Description</span><span class="sxs-lookup"><span data-stu-id="9255a-107">Description</span></span></th>
<th><span data-ttu-id="9255a-108">支援的介面</span><span class="sxs-lookup"><span data-stu-id="9255a-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9255a-109"><strong>類別</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="9255a-110">表示類別定義的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="9255a-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>得到 iadsclass</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-112"><strong>電腦</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="9255a-113">代表電腦的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="9255a-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-115"><strong>網域</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="9255a-116">透過網路表示網域的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="9255a-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="9255a-119">代表檔案服務的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="9255a-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="9255a-122">代表檔案共用的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="9255a-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-124"><strong>FPNWFileService</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="9255a-125">代表檔案服務的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="9255a-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-127"><strong>FPNWFileShare</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="9255a-128">代表檔案共用的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="9255a-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-130"><strong>FPNWResource</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="9255a-131">代表資源的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="9255a-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-133"><strong>FPNWResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-134">代表資源集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="9255a-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-136"><strong>FPNWSession</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="9255a-137">表示會話的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="9255a-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-139"><strong>FPNWSessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-140">表示會話集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="9255a-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-142"><strong>群組</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="9255a-143">代表群組的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="9255a-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="9255a-145">GetInfo 不能用於包含在 WinNT 範圍中 W w n 安全性主體之成員的群組。</span><span class="sxs-lookup"><span data-stu-id="9255a-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-147">表示群組集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="9255a-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-149"><strong>LocalGroup</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="9255a-150">表示本機群組的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="9255a-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-152"><strong>LocalgroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-153">表示本機群組集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="9255a-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-155"><strong>Namespace</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="9255a-156">表示 WinNT 命名空間的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="9255a-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="9255a-159">表示列印工作的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="9255a-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-161"><strong>PrintJobsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-162">表示列印工作集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="9255a-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="9255a-165">表示列印佇列的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="9255a-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-167"><strong>屬性</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="9255a-168">表示屬性定義的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="9255a-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-170"><strong>Resource</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="9255a-171">代表資源的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="9255a-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-173"><strong>ResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-174">代表資源集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="9255a-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-176"><strong>結構描述</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="9255a-177">表示架構容器的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="9255a-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-179"><strong>服務</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="9255a-180">代表服務的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="9255a-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-182"><strong>工作階段</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="9255a-183">表示會話的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="9255a-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-185"><strong>SessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-186">表示會話集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="9255a-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-188"><strong>語法</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="9255a-189">表示屬性語法的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="9255a-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9255a-191"><strong>使用者</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="9255a-192">表示使用者帳戶的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="9255a-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="9255a-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9255a-194"><strong>UserGroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9255a-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="9255a-195">表示使用者群組集合的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="9255a-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="9255a-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="9255a-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





