---
title: 64 位元 Windows 程式設計手冊
description: Microsoft 發行了64位版本的 Windows 作業系統。
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，首頁
- 64位 Windows 64 位 Windows 程式設計的程式設計指南，請參閱64位 Windows 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743465"
---
# <a name="programming-guide-for-64-bit-windows"></a>64 位元 Windows 程式設計手冊

Microsoft 發行了64位版本的 Windows 作業系統。 64位 Windows 是以相容性來設計的。 開發人員可確保其現有的32位應用程式在64位 Windows 下正常執行，或藉由遷移其應用程式來利用64位 Windows 的優點。

## <a name="benefits-of-64-bit-windows"></a>64位 Windows 的優點

64位作業系統支援的實體記憶體遠高於32位作業系統。 例如，大部分的32位 Windows 系統最多可支援 4 gb 的實體記憶體，每個進程最多可有 3 gb 的位址空間，而64位 Windows 最多可支援 2 tb 的實體記憶體，而且每個進程都有 8 tb 的位址空間。 增加的實體記憶體包含應用程式的下列優點：

-   每個應用程式都可以支援更多使用者。 每個使用者都必須複寫每個應用程式的所有或部分，而這需要額外的記憶體。
-   每個應用程式都有更好的效能。 增加的實體記憶體可讓更多的應用程式同時執行，並保持在系統的主要記憶體中。 這可減少或消除在磁片之間交換頁面的效能負面影響。
-   每個應用程式都有更多記憶體來儲存及運算元據。 資料庫可以在系統的實體記憶體中儲存更多的資料。 資料存取速度較快，因為不需要磁片讀取。
-   應用程式可以輕鬆且更可靠地處理大量資料。 移動圖片工作的影片組合需要64位 Windows 因此原因。 科學與財務應用程式的模型化可大幅提升記憶體常駐資料結構，而不可能在32位 Windows 上。

企業也有很重要的優點：

-   提高生產力。 知識工作者可以花時間思考和產生，而不是等待軟體完成其工作。
-   降低所有權的成本。 每部伺服器可以支援更大量的使用者和應用程式，因此您的企業需要較少的伺服器。 這會直接轉譯為較少的管理額外負荷，也就是任何運算環境中最高的成本之一。
-   新的應用程式機會。 您可以設計新的應用程式，而不會有32位 Windows 所加諸的阻礙。 新的圖形應用程式可讓工作變得更簡單且更愉快。 目前無法使用的資料密集工作，可透過64位 Windows 完成。

## <a name="in-this-section"></a>本章節內容

-   [準備開始進行64位 Windows](getting-ready-for-64-bit-windows.md)
-   [設計64位相容介面](designing-64-bit-compatible-interfaces.md)
-   [執行32位應用程式](running-32-bit-applications.md)
-   [移轉提示](migration-tips.md)

 

 




