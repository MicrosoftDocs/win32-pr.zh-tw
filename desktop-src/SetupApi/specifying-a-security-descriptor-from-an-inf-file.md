---
description: 您可以控制進程存取安全物件或執行系統管理工作的能力。
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: 從 INF 檔案指定安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945244"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="e38c2-103">從 INF 檔案指定安全描述項</span><span class="sxs-lookup"><span data-stu-id="e38c2-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="e38c2-104">您可以控制進程存取安全物件或執行系統管理工作的能力。</span><span class="sxs-lookup"><span data-stu-id="e38c2-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="e38c2-105">安全物件是可以有安全描述項的物件。</span><span class="sxs-lookup"><span data-stu-id="e38c2-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="e38c2-106">所有命名物件都是安全的。</span><span class="sxs-lookup"><span data-stu-id="e38c2-106">All named objects are securable.</span></span> <span data-ttu-id="e38c2-107">某些未命名的物件（例如處理常式和執行緒物件）也可以有安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e38c2-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="e38c2-108">如需控制安全物件存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="e38c2-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="e38c2-109">[安全描述項](/windows/desktop/SecAuthZ/security-descriptors) 包含與安全物件相關聯的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="e38c2-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="e38c2-110">對於大部分的安全物件而言，您可以在建立物件的函式呼叫中指定物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e38c2-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="e38c2-111">例如，您可以在 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數中指定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e38c2-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="e38c2-112">若要從 INF 檔案設定安全描述項，請在安裝檔案、登錄機碼或元件的區段之後，立即新增 [INF 寫入器撰寫的安全性] 區段。</span><span class="sxs-lookup"><span data-stu-id="e38c2-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="e38c2-113">[安全性] 區段應該包含一行，其中包含使用 [安全描述項字串](/windows/desktop/SecAuthZ/security-descriptor-strings)的格式寫入的字串安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e38c2-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="e38c2-114">該行也應以引號括住 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="e38c2-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="e38c2-115">例如，下列 INF 檔案程式碼片段會建立只有系統管理員和系統可存取的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e38c2-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="e38c2-116">請注意，此範例需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="e38c2-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="e38c2-117">在此情況下，字串的意義是系統管理員有完全控制、系統具有完整控制權，而且存取權可繼承至所有子機碼。</span><span class="sxs-lookup"><span data-stu-id="e38c2-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="e38c2-118">如需詳細資訊，請參閱 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)。</span><span class="sxs-lookup"><span data-stu-id="e38c2-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
