---
title: WOW64 下的記憶體管理
description: WOW64 下的記憶體管理取決於處理器架構。
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 位 Windows 程式設計，記憶體管理
- 記憶體管理 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132831"
---
# <a name="memory-management-under-wow64"></a>WOW64 下的記憶體管理

WOW64 下的記憶體管理取決於處理器架構。

## <a name="itanium-support"></a>Itanium 支援

WOW64 會在 Itanium 處理器所使用的原生 8 KB 頁面上模擬 4 KB 的頁面。 處理器藉由提供具有低額外負荷的絕佳模擬來提供協助。 模擬程式碼無法處理下列案例：

-   寫入追蹤。 [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch)和 [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch)函式會使用原生頁面大小的資料細微性在核心中執行，這表示 WOW64 4 kb 頁面模擬無法判斷在基礎 8 kb 頁面中寫入哪些模擬的 4 kb 頁面。
-   [處理 (AWE) 的視窗化延伸 ](/windows/desktop/Memory/address-windowing-extensions)模組。 AWE 函式是在頁碼上操作，而且沒有任何方法可將64位頁碼對應到32位頁碼。
-   區段對齊。 針對區段對齊小於 8 KB 的可執行映射 (預設為 4 KB 的 x86 映射) ，WOW64 必須中途變更所有的影像頁面。 這可有效地將每一頁複製到分頁檔，並防止在進程間共用唯讀影像頁面。
-   不支援 [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) 和 [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) 函數。

## <a name="x64-and-arm64-support"></a>x64 和 ARM64 支援

原生頁面大小為 4 KB。 因此，支援下列各項：

-   支援 [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) 和 [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) 函數。
-   支援 [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) 和 [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) 函數。
-   使用大型位址有一些優點，因為 x64 WOW64 支援 4 GB 的虛擬位址空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 版本的記憶體限制](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[4 GT RAM 調整](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 