---
description: 安裝程式會將使用者介面的所有資訊儲存在安裝資料庫的資料表中。
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: 預覽消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193101"
---
# <a name="previewing-the-user-interface"></a>預覽消費者介面

安裝程式會將 [使用者介面](user-interface.md) 的所有資訊儲存在安裝資料庫的資料表中。 為了加速 UI 的設計，安裝程式也會提供預覽模式來查看這項資訊。 下列程式描述如何啟用 UI 預覽模式，並顯示對話方塊和公告欄目前的外觀。

**在預覽模式中查看使用者介面**

1.  藉由呼叫 [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) 函數來啟用預覽模式。
2.  藉由呼叫 [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) 函數來顯示特定的對話方塊。
3.  藉由呼叫 [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) 函數來顯示特定公告欄。

 

 



