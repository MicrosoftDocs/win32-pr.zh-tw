---
description: 管道伺服器會在 CreateNamedPipe 函數的 dwOpenMode 參數中，指定管道存取、重迭和寫入模式。 管道用戶端可以使用 CreateFile 函式，為管道控制碼指定這些開啟模式。
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: 具名管道開啟模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7fe3f843a157e69d8b938630e5eb9efa95035960cb6578325be6bddd5d93c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451258"
---
# <a name="named-pipe-open-modes"></a>具名管道開啟模式

管道伺服器會在 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)函數的 *dwOpenMode* 參數中，指定管道存取、重迭和寫入模式。 管道用戶端可以使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式，為管道控制碼指定這些開啟模式。

## <a name="access-mode"></a>存取模式

設定管道存取模式相當於指定與管道伺服器控制碼相關聯的讀取或寫入存取權。 下錶針對您可以使用 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)指定的每個存取模式，顯示對等的一般存取許可權。



| 存取模式            | 對等的一般存取權限 |
|------------------------|---------------------------------|
| 管道 \_ 存取 \_ 輸入  | 一般 \_ 讀取                   |
| 管道 \_ 存取 \_ 輸出 | 一般 \_ 寫入                  |
| 管道 \_ 存取 \_ 雙工   | 泛型 \_ 讀取 \| 一般 \_ 寫入 |



 

如果管道伺服器使用管道存取輸入建立管道 \_ \_ ，管道伺服器的管道會是唯讀的，而管道用戶端的管道則是唯讀的。 如果管道伺服器建立了具有管道存取輸出的管道，則管道 \_ \_ 是僅針對管道伺服器的寫入，而管道用戶端的唯讀。 使用管道 \_ 存取雙工建立的管道 \_ 是管道伺服器和管道用戶端的讀取/寫入。

使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 連接到具名管道的管道用戶端，必須在 *dwDesiredAccess* 參數中指定與管道伺服器所指定之存取模式相容的存取權限。 例如，用戶端必須指定一般 \_ 讀取權限，才能開啟管道伺服器使用 [管道存取輸出] 建立的管道句 \_ 柄 \_ 。 所有管道實例的存取模式都必須相同。

若要讀取管道屬性（例如讀取模式或封鎖模式），管道控制碼必須具有 [檔案 \_ 讀取 \_ 屬性] 存取權限; 若要寫入管道屬性，管道控制碼必須有 [檔案 \_ 寫入屬性] 存取權限 \_ 。 這些存取權限可以與適用于管道的一般存取權限結合：適用于 \_ 唯讀管道的一般讀取和檔案 \_ 寫入 \_ 屬性，或 \_ \_ \_ 僅限寫入管道的一般寫入與檔案讀取屬性。 以這種方式限制存取權限可提供更佳的管道安全性。

## <a name="overlapped-mode"></a>重迭模式

在重迭模式中，執行長時間讀取、寫入和連接作業的函式可能會立即返回。 這可讓執行緒在背景中執行耗時的作業時，執行其他作業。 若要指定重迭模式，請使用檔案旗標重迭 \_ \_ 旗標。 如需詳細資訊，請參閱 [同步和重迭的輸入和輸出](synchronous-and-overlapped-input-and-output.md)。

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式可讓管道用戶端 \_ \_ 使用 *dwFlagsAndAttributes* 參數，為其管道控制碼設定重迭模式 (檔旗標重迭) 。

## <a name="write-through-mode"></a>Write-Through 模式

\_透過檔案旗標 \_ 寫入來指定寫入模式 \_ 。 此模式只會影響在不同電腦上的管道用戶端與管道伺服器之間的位元組類型管道的寫入作業。 在寫入模式中，寫入具名管道的函式不會傳回，直到資料透過網路傳輸到遠端電腦上的管道緩衝區為止。 寫入模式適用于需要每次寫入作業進行同步處理的應用程式。

如果未啟用寫入模式，系統會緩衝處理資料，以增強網路作業的效率，直到最小的位元組數目已累積，或直到最大時間週期經過為止。 緩衝可讓系統將多個寫入作業結合成單一網路傳輸。 這表示當系統將資料放在輸出緩衝區中，但在系統將資料傳輸到網路上之前，寫入作業可以順利完成。

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式可讓管道用戶端使用 dwFlagsAndAttributes 參數，將寫入模式 (檔案 \_ 旗標 \_ 寫入 \_ 至其管道控制碼的) 。 建立管道控制碼之後，無法變更管道控制碼的寫入模式。 針對相同管道實例的伺服器和用戶端控制碼，寫入模式可能會不同。

管道用戶端可以使用 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式來控制已停用寫入模式之管道的傳輸之前的位元組數和超時時間。 若為唯讀管道，必須以「一般讀取」和「檔案 \_ \_ 寫入屬性」存取權限開啟管道控制碼 \_ 。

 

 
