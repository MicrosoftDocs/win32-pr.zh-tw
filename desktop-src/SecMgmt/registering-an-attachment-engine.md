---
description: 在安全性設定引擎可以呼叫您的附件引擎來處理服務特定工作之前，您必須先安裝附件引擎，並向安全性設定引擎註冊。
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: 註冊附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000241"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="d6eef-103">註冊附件引擎</span><span class="sxs-lookup"><span data-stu-id="d6eef-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="d6eef-104">在安全性設定引擎可以呼叫您的附件引擎來處理服務特定工作之前，您必須先安裝附件引擎，並向安全性設定引擎註冊。</span><span class="sxs-lookup"><span data-stu-id="d6eef-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="d6eef-105">**安裝並註冊附件引擎 DLL**</span><span class="sxs-lookup"><span data-stu-id="d6eef-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="d6eef-106">將附件引擎 DLL 複製到系統上的目錄。</span><span class="sxs-lookup"><span data-stu-id="d6eef-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="d6eef-107">慣用的目錄為% windir% \\ secedit 個 \\ 附件。</span><span class="sxs-lookup"><span data-stu-id="d6eef-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="d6eef-108">如果此目錄不存在，您應該建立它。</span><span class="sxs-lookup"><span data-stu-id="d6eef-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="d6eef-109">在下列節點底下建立登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d6eef-109">Create a registry key under the following node.</span></span> <span data-ttu-id="d6eef-110">*服務名稱* 是附件的註冊名稱，而且必須是服務控制管理員中所使用的相同服務名稱，也就是管理服務停止和啟動的模組。</span><span class="sxs-lookup"><span data-stu-id="d6eef-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="d6eef-111">名稱也必須是唯一的，因此它不會與其他附件的名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="d6eef-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="d6eef-112">在新的登錄機碼中建立下列字串值。</span><span class="sxs-lookup"><span data-stu-id="d6eef-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="d6eef-113">*附件引擎路徑* 是附件引擎模組的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d6eef-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="d6eef-114">**ServiceAttachmentPath**  = *附件引擎路徑*</span><span class="sxs-lookup"><span data-stu-id="d6eef-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="d6eef-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="d6eef-115">Data type</span></span>
</dt> <dd><span data-ttu-id="d6eef-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d6eef-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



