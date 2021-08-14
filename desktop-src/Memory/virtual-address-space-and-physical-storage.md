---
description: Microsoft Windows 所支援的最大實體記憶體數量，從 2 GB 到 2 TB 的範圍，視 Windows 的版本而定。
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: 虛擬位址空間和實體儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 774e0af302fbd965f16b09a88d6dabb7c95948855c8d939d3c856ebe098337d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386153"
---
# <a name="virtual-address-space-and-physical-storage"></a>虛擬位址空間和實體儲存體

Microsoft Windows 所支援的最大實體記憶體數量，從 2 GB 到 24 TB 的範圍，視 Windows 的版本而定。 如需詳細資訊，請參閱[Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。 每個進程的虛擬位址空間可小於或大於電腦上可用的實體記憶體總數。 位於實體記憶體之進程的虛擬位址空間子集，稱為 *工作集*。 如果進程的執行緒嘗試使用的實體記憶體多於目前可用的實體記憶體，系統會將一些記憶體內容分頁至磁片。 進程可用的虛擬位址空間總數量受限於可供分頁檔使用的實體記憶體和可用磁碟空間。

實體儲存體和每個進程的虛擬位址空間會組織成 *頁面*（記憶體單位），其大小取決於主機電腦。 例如，在 x86 電腦上，主機頁面大小為 4 kb。

為了充分發揮其管理記憶體的彈性，系統可以將實體記憶體的頁面移入和移出磁片上的分頁檔。 當頁面在實體記憶體中移動時，系統會更新受影響之進程的頁面對應。 當系統需要實體記憶體中的空間時，會將最近使用的實體記憶體分頁移至分頁檔案。 系統對實體記憶體的操作對應用程式而言是完全透明的，只會在其虛擬位址空間中操作。

 

 



