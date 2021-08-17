---
description: 檔案系統辨識的目標是要讓 Windows 作業系統能夠針對有效但無法辨識的檔案系統提供額外的選項，而非 &\# 0034;原始&\# 0034;。
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: 檔案系統識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cf33e8a6e3378ad5b9f0123cb78fa228b5b780e7440a2981b10982e76d187a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996955"
---
# <a name="file-system-recognition"></a>檔案系統識別

檔案系統辨識的目標是要讓 Windows 作業系統能夠針對有效但無法辨識的檔案系統提供額外的選項，而非「原始」。 為了達成此目的，從 Windows 7 和 Windows Server 2008 R2 開始，系統會定義固定的資料結構類型，此類型可寫入至已啟用變更檔案系統格式之技術的媒體。 此資料結構（如果存在於邏輯磁片磁區0）將會被作業系統辨識，並通知使用者媒體包含有效但無法辨識的檔案系統，而且如果未安裝檔案系統的驅動程式，則不是原始卷。

## <a name="file-system-recognition-features-and-use"></a>檔案系統識別功能與使用

許多最近的儲存技術已改變磁片上檔案系統格式，使這些技術啟用的媒體無法辨識至舊版 Windows，因為檔案系統驅動程式在特定舊版的 Windows 發行時不存在。 此案例中先前的預設行為如下所示。 當存放裝置媒體不是已知的檔案系統時，它會被識別為 RAW，然後傳播至 Windows Shell，其中會以使用者介面 (UI) 的格式自動播放提示。 如果新檔案系統的作者正確地將適當的 [**資料結構**](file-system-recognition-structure.md) 寫入磁片，檔案系統辨識可解決此問題。

檔案系統識別會在作業系統內使用下列功能和層級，以達成其目標：

-   儲存體媒體，其中固定的資料結構會以一系列的位元組順序存在，這些位元組會在內部以預先定義的結構（稱為 [**檔 \_ 系統辨識 \_ \_ 結構**](file-system-recognition-structure.md)資料結構）排列。 檔案系統開發人員必須負責適當地建立此磁片上的結構。
-   應用層級的檔案系統識別，透過使用 [**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) 裝置 i/o 控制程式代碼來達成。 如需如何使用此控制項程式碼的範例，請參閱 [取得檔案系統識別資訊](obtaining-file-system-recognition-information.md)。
-   總和檢查碼驗證碼，儲存在 [**檔 \_ 系統 \_ 識別 \_ 結構**](file-system-recognition-structure.md) 資料結構內。 如需如何計算此總和檢查碼的範例，請參閱 [計算檔案系統識別總和檢查](computing-a-file-system-recognition-checksum.md)碼。
-   Windows Shell UI 使用先前列出的功能，為無法辨識的檔案系統提供更具彈性且健全的自動播放和相關支援，但只有當 [**檔 \_ 系統 \_ 辨識 \_ 結構**](file-system-recognition-structure.md)資料結構存在於邏輯磁片磁區零時，才能運作。 執行新檔案系統的開發人員應該利用這個系統來確保其檔案系統不會被誤假設為「RAW」類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計算檔案系統識別總和檢查碼](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[取得檔案系統識別資訊](obtaining-file-system-recognition-information.md)
</dt> <dt>

[取得磁片區資訊](obtaining-volume-information.md)
</dt> </dl>

 

 
