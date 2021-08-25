---
description: 在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個壓縮屬性。
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: 壓縮屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99fb42aaa30fc3e5d2ef36da85bae194950c587d024510b18233f3c83504ab88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982148"
---
# <a name="compression-attribute"></a>壓縮屬性

在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個 *壓縮屬性*。 其他檔案系統也可以針對個別檔案和目錄執行壓縮屬性。

您可以藉由呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式並檢查 **檔案 \_ \_ 壓縮** 位旗標，判斷檔案系統是否支援檔案和目錄的壓縮屬性。

使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 或 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) 函數來判斷檔案或目錄的壓縮屬性。

如果檔案的壓縮屬性設定 (**檔 \_ 屬性 \_ 壓縮**) ，則會壓縮檔案中的所有資料。 如果屬性為清除，則不會壓縮檔案中的任何資料。 從使用者模式程式設計觀點來看，沒有部分壓縮的狀態;壓縮屬性是壓縮狀態的簡單布林指標。

目錄的壓縮屬性為新建立的檔案和子目錄提供預設的壓縮屬性。 當您呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 或 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 來建立新的檔案或目錄時，新的檔案或目錄會繼承其父目錄的壓縮屬性。

若要修改檔案或目錄的 **檔 \_ 屬性 \_ 壓縮** 屬性，您必須搭配使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式和 [**FSCTL \_ SET \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) 控制程式代碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案屬性常數**](file-attribute-constants.md)
</dt> </dl>

 

 
