---
description: 應用程式可透過程式設計方式建立和刪除目錄。
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: 建立和刪除目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114337"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="935f9-103">建立和刪除目錄</span><span class="sxs-lookup"><span data-stu-id="935f9-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="935f9-104">應用程式可透過程式設計方式建立和刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="935f9-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="935f9-105">若要建立新的目錄，請使用 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)、 [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)或 [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) 函數。</span><span class="sxs-lookup"><span data-stu-id="935f9-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="935f9-106">建立目錄時，會指定目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="935f9-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="935f9-107">命名目錄的慣例遵循命名檔案的慣例。</span><span class="sxs-lookup"><span data-stu-id="935f9-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="935f9-108">如需這些慣例的說明，請參閱 [命名](naming-a-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="935f9-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="935f9-109">若要刪除現有的目錄，請使用 [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) 或 [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) 函數。</span><span class="sxs-lookup"><span data-stu-id="935f9-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="935f9-110">移除目錄之前，您必須確定目錄是空的，而且您擁有該目錄的 [刪除] 存取權限。</span><span class="sxs-lookup"><span data-stu-id="935f9-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="935f9-111">若要這樣做，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="935f9-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
