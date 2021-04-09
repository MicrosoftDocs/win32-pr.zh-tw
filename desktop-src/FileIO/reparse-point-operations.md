---
description: 描述您可以使用 DeviceIoControl 執行的重新分析點作業。
ms.assetid: c7279203-2443-401e-b541-038954094266
title: 重新分析點作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027258"
---
# <a name="reparse-point-operations"></a>重新分析點作業

若要判斷檔案系統是否支援重新分析點，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式，並檢查檔案是否 **支援重新 \_ \_ 分析 \_ 點** 位旗標。

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數可讓您設定、修改、取得和移除重新分析點。 下表描述您可以使用 **DeviceIoControl** 執行的重新分析點作業。



| 作業                                                           | 描述                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**FSCTL \_ 設定重新 \_ 分析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | 允許呼叫程式設定新的重新分析點，或修改現有的重新分析點。<br/> |
| [**FSCTL \_ 取得重新 \_ 剖析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | 取得儲存在現有重新分析點中的資訊。<br/>                         |
| [**FSCTL \_ 刪除重新 \_ 分析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | 移除現有的重新分析點。<br/>                                                   |



 

如果您要修改、取得或刪除重新分析點，您必須在檔案所包含的作業中指定相同的重新分析標記。 否則，作業將會失敗，並出現錯誤重新 **\_ 分析 \_ 標記 \_ 不符** 的錯誤。 如果您要修改或刪除重新分析點，您也必須在檔案所包含的作業中指定重新分析 **GUID** 。 否則，作業將會失敗，並出現錯誤重新 **\_ 分析 \_ 屬性 \_ 衝突**。

若要判斷檔案或目錄是否包含重新分析點，請使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函數。 如果檔案或目錄有相關聯的重新分析點，則會設定 **檔 \_ 屬性重新 \_ 分析 \_ 點** 屬性。

若要覆寫現有的重新分析點，而不使用檔案或目錄的控制碼，請使用檔案 **\_ 旗標開啟重新 \_ \_ 分析 \_ 點** 來呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 。 這個旗標可讓您開啟檔案，無論對應的檔案系統篩選器是否已安裝且正常運作。

 

