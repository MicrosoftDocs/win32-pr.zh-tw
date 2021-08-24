---
description: 對話方塊是在對話方塊資料表的對話方塊資料行中指定。 如需在使用者介面中新增對話方塊或佈告欄的詳細資訊，請參閱使用消費者介面。
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: '對話方塊 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38da0e4d562854abc32064eee06a303747c2587591a5526ae98177a13e0462a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764058"
---
# <a name="dialog-boxes-windows-installer"></a>對話方塊 (Windows Installer) 

對話方塊是在 [對話方塊資料表](dialog-table.md)的對話方塊資料行中指定。 如需在使用者介面中新增對話方塊或佈告欄的詳細資訊，請參閱 [使用消費者介面](using-the-user-interface.md)。

## <a name="reserved-dialog-box-names"></a>保留的對話方塊名稱

下列對話方塊名稱是由 Windows Installer 保留，不能用於任何使用者撰寫的自訂對話方塊。 安裝程式會要求在 [對話方塊資料表](dialog-table.md) 中，使用下列保留名稱來列出這些對話方塊。 每個對話方塊和名稱只能列出一次。 開發人員必須在使用者介面中撰寫這些對話方塊。 如需如何預覽對話方塊的詳細資訊，請參閱匯 [入消費者介面](importing-the-user-interface.md)。



| 對話方塊名稱                                      | 對話方塊的簡短描述                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FilesInUse 對話方塊](filesinuse-dialog.md)           | 警示使用者進程覆寫或刪除檔案。                                                                                                                 |
| [Firstrun.cmd 對話方塊](firstrun-dialog.md)               | 收集使用者名稱、公司名稱和產品識別碼。                                                                                                                       |
| [MsiRMFilesInUse 對話方塊](msirmfilesinuse-dialog.md) | 警示使用者處理覆寫或刪除檔案，並讓使用者可以選擇使用 [重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal) 來關閉和重新開機應用程式。 |



 

## <a name="required-dialog-boxes"></a>必要對話方塊

在安裝期間，某些事件會導致 Windows Installer 檢查封裝中的[使用者介面順序資料表](using-a-sequence-table.md)，並顯示指定的對話方塊。 例如，在發生嚴重錯誤的情況下，Windows Installer 會顯示在使用者介面順序資料表中，以-3 序號列出的對話方塊，不論對話方塊[資料表](dialog-table.md)中該對話方塊的名稱為何。 下表列出特定事件，以及其在使用者介面順序資料表中的對應序號：



| 事件種類                        | 使用者介面順序資料表序號 | 對話方塊的描述                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [嚴重錯誤](fatalerror-dialog.md) | -3                                            | 安裝因嚴重錯誤而終止。      |
| [使用者離開](userexit-dialog.md)     | -2                                            | 已在使用者的要求結束安裝。 |
| [結束](exit-dialog.md)              | -1                                            | 安裝已順利完成。               |



 

此外，封裝作者必須建立一般對話方塊來顯示 Windows Installer[錯誤](error-dialog.md)訊息。 此對話方塊可以命名為任何名稱，但必須在 **ErrorDialog** 屬性中指定這個名稱。

## <a name="typical-dialog-boxes"></a>一般對話方塊

下列對話方塊是選擇性的，通常包含在安裝套件的撰寫使用者介面中。 這些對話方塊通常是安裝檔案的大部分 [使用者介面嚮導](user-interface-wizard-behavior.md) 。 這些對話方塊在對話方塊資料表中可以有任何名稱。 所顯示的名稱只建議用來清楚起見，而且可以視需要進行修改。 例如，您可以在封裝中使用兩個不同的自訂 **LicenseAgreement** 對話方塊，並依名稱 ProfessionalLicenseAgreement 和 LimitedLicenseAgreement 來辨別對話方塊資料表。



| 對話方塊類型                                             | 對話方塊的簡短描述                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [DiskCost 對話方塊](diskcost-dialog.md)                  | 指出沒有足夠的磁碟空間可供安裝。 |
| [瀏覽對話方塊](browse-dialog.md)                      | 可讓使用者選取目錄。                     |
| [取消對話方塊](cancel-dialog.md)                      | 確認終止安裝的要求。       |
| [授權合約對話方塊](licenseagreement-dialog.md) | 顯示授權合約的模式方塊。             |
| [選取對話方塊](selection-dialog.md)                | 讓使用者選取專案的模式方塊。            |



 

 

 
