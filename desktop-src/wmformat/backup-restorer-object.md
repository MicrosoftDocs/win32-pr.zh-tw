---
title: Backup Restorer 物件
description: Backup Restorer 物件
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media 格式 SDK，備份 restorer 物件
- Advanced Systems Format (ASF) 、backup restorer 物件
- ASF (Advanced Systems Format) ，backup restorer 物件
- 物件、備份 restorer 物件
- 備份 restorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106967244"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="802b0-108">Backup Restorer 物件</span><span class="sxs-lookup"><span data-stu-id="802b0-108">Backup Restorer Object</span></span>

<span data-ttu-id="802b0-109">備份 restorer 提供介面來處理備份授權（通常是移至卸載式媒體），然後將這些授權還原到新的電腦上。</span><span class="sxs-lookup"><span data-stu-id="802b0-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="802b0-110">Backup restorer 物件是由 [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) 函數所建立，它會設定 [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="802b0-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="802b0-111">您可以藉由呼叫 **QueryInterface** 方法來取得 backup restorer 物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="802b0-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="802b0-112">Backup restorer 物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="802b0-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="802b0-113">介面</span><span class="sxs-lookup"><span data-stu-id="802b0-113">Interface</span></span>                                              | <span data-ttu-id="802b0-114">描述</span><span class="sxs-lookup"><span data-stu-id="802b0-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="802b0-115">**IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="802b0-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="802b0-116">設定及抓取 [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) 和 [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) 介面所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="802b0-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="802b0-117">**IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="802b0-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="802b0-118">備份授權，通常可將其還原到另一部電腦上。</span><span class="sxs-lookup"><span data-stu-id="802b0-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="802b0-119">**IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="802b0-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="802b0-120">還原授權。</span><span class="sxs-lookup"><span data-stu-id="802b0-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="802b0-121">下列回呼介面必須由應用程式執行，才能使用 backup restorer 物件。</span><span class="sxs-lookup"><span data-stu-id="802b0-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="802b0-122">介面</span><span class="sxs-lookup"><span data-stu-id="802b0-122">Interface</span></span>                                      | <span data-ttu-id="802b0-123">描述</span><span class="sxs-lookup"><span data-stu-id="802b0-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="802b0-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="802b0-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="802b0-125">接收在個別執行緒中執行之進程的狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="802b0-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="802b0-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="802b0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="802b0-127">**備份和還原授權**</span><span class="sxs-lookup"><span data-stu-id="802b0-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="802b0-128">**物件**</span><span class="sxs-lookup"><span data-stu-id="802b0-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




