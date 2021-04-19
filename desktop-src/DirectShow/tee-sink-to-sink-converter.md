---
description: T/接收到接收轉換器
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: T/接收到接收轉換器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979820"
---
# <a name="teesink-to-sink-converter"></a>T/接收到接收轉換器

端對端/接收到接收轉換器是以核心模式、KsProxy 為基礎的篩選。 它用於轉譯或捕獲 VBI 資料的類比視頻電視篩選圖形中。 篩選會連接上游至 [WDM 影片捕獲篩選器](wdm-video-capture-filter.md) ，並提供有效率的方法來複製核心模式中的資料流程，而不需要在核心和使用者模式之間進行昂貴的轉換。 它會將每個接收到的資料區塊傳遞給所有輸出圖釘，而下游編解碼器會負責尋找要解碼的特定 VBI 資料。

端對端對接收的轉換器會出現在「WDM 串流的 t/分隔裝置」篩選類別 (AM \_ KSCATEGORY \_ 分隔器) 。

由於這是核心模式篩選器，因此應用程式無法直接使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立它。 相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。 如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 
