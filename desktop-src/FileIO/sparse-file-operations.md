---
description: 藉由呼叫 GetVolumeInformation 函數，判斷檔案系統是否支援稀疏檔案。
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: 稀疏檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9835d550a414c047e578eb90fc9b55afbefb760d31d8333a290f00da7162f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015106"
---
# <a name="sparse-file-operations"></a>稀疏檔案作業

若要判斷檔案系統是否支援稀疏檔案，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函式，並檢查檔案是否支援透過 *lpFileSystemFlags* 參數傳回的 **\_ \_ 稀疏 \_** 檔案位旗標。

大部分的應用程式不會察覺到稀疏檔案，也不會建立稀疏檔案。 應用程式讀取稀疏檔案的事實是應用程式的透明。 知道稀疏檔案的應用程式應該要判斷其資料集是否適合保存在稀疏檔案中。 進行這項判斷之後，應用程式必須使用 [**FSCTL \_ SET \_ sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) control 程式碼，將檔案明確宣告為稀疏。

應用程式將檔案設定為稀疏之後，應用程式就可以使用 [**FSCTL \_ set \_ zero \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) control 程式碼，將檔案的區域設定為零。 此外，應用程式可以使用已配置 [**的 \_ FSCTL \_ 查詢 \_ 範圍**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) 控制程式代碼，以加快搜尋稀疏檔案中非零資料的速度。

當您使用 [**FSCTL \_ SET \_ ZERO \_ data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) 以外的函式或作業來執行 (寫入作業時，如果資料不是由零所組成，則會將整個寫入長度寫入磁片。 若要從零移出檔案範圍並維持疏鬆度，請使用 **FSCTL \_ 設定零的 \_ \_ 資料**。

疏鬆度感知的應用程式可能也會將現有的檔案設定為稀疏。 如果應用程式將現有的檔案設定為稀疏，則應該針對包含零的區域掃描該檔案，然後使用 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) 來重設這些區域，因此可能會解除配置某些實體磁片儲存體。 升級為稀疏檔案感知的應用程式應該執行這種轉換。

當您從稀疏檔案的清空部分執行讀取作業時，作業系統可能無法從硬碟讀取。 相反地，系統會辨識要讀取之檔案的部分包含零，並傳回已滿零的緩衝區，而不會實際讀取磁片。

就像任何其他檔案一樣，系統也可以將資料寫入至稀疏檔案中的任何位置或從中讀取資料。 寫入至先前的已清空檔案部分的非零資料可能會導致配置磁碟空間。 使用非零資料寫入零 (只有 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) 可能會導致磁碟空間解除配置。

> [!Note]  
> 藉由在 [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)的情況下寫入零，應用程式就能維護疏鬆度。

 

在 NTFS 檔案系統上處理壓縮檔案的磁碟重組工具，將會正確處理 NTFS 檔案系統磁片區上的稀疏檔。 在使用可用空間之前，大型且高度分散的稀疏檔案可能會超過磁片範圍的 NTFS 限制。 如需詳細資訊，請參閱 [擴充檔案可能會因為「磁片已滿」錯誤而失敗，即使磁片區具有可用空間也一樣](https://support.microsoft.com/default.aspx/kb/957180)。

 

 
