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
# <a name="backup-restorer-object"></a>Backup Restorer 物件

備份 restorer 提供介面來處理備份授權（通常是移至卸載式媒體），然後將這些授權還原到新的電腦上。

Backup restorer 物件是由 [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) 函數所建立，它會設定 [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) 介面的指標。 您可以藉由呼叫 **QueryInterface** 方法來取得 backup restorer 物件的其他介面。

Backup restorer 物件支援下列介面。



| 介面                                              | 描述                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | 設定及抓取 [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) 和 [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) 介面所需的屬性。 |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | 備份授權，通常可將其還原到另一部電腦上。                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | 還原授權。                                                                                                                                        |



 

下列回呼介面必須由應用程式執行，才能使用 backup restorer 物件。



| 介面                                      | 描述                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 接收在個別執行緒中執行之進程的狀態訊息。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**備份和還原授權**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**物件**](objects.md)
</dt> </dl>

 

 




