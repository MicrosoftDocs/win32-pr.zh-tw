---
description: PGM 使用通訊端選項來設定狀態、提供多播參數，並以其他方式執行其多播功能。
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: PGM 通訊端選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848004"
---
# <a name="pgm-socket-options"></a>PGM 通訊端選項

PGM 使用通訊端選項來設定狀態、提供多播參數，並以其他方式執行其多播功能。 此頁面指定應如何設定 PGM 通訊端選項、列舉適用于 PGM 的通訊端選項，以及在適當的情況下，提供各種選項的使用範例和其他資訊。 如需每個 PCM 通訊端選項的基本定義，請參閱 [通訊端選項](socket-options.md)。

**WINDOWS XP：** 不支援可靠的多播程式設計 (的 PGM) 。

下列通訊端選項適用于 PGM 寄件者：

<dl> RM \_ LATEJOIN  
RM \_ 速率 \_ 視窗 \_ 大小  
RM \_ 傳送 \_ 視窗 \_ 進階 \_ 率  
RM 傳送者 \_ \_ 統計資料  
RM 傳送者 \_ \_ 視窗 \_ 前進 \_ 方法  
RM \_ SET \_ MCAST \_ TTL  
RM \_ 設定 \_ 訊息 \_ 界限  
RM \_ 設定 \_ 傳送 \_ IF  
RM \_ 使用 \_ FEC  
</dl>

[RM \_ \_ 傳送者] 視窗 [ \_ 前進方法] 選項會指定在 \_ 前進尾端 edge 傳送視窗時所使用的方法。 Optval 參數只能透過 \_ \_ \_ (預設) 的時間，以電子視窗前進 \_ 。 請注意， \_ \_ 不支援使用 E 視窗 \_ 作為資料快取 \_ \_ 。

以下是適用于 PGM 接收器的通訊端選項：

<dl> RM \_ 新增 \_ 接收（ \_ 如果  
RM \_ DEL \_ 接收 \_  
RM \_ 高速 \_ \_ 內部網路 \_ 選擇  
RM \_ 接收器 \_ 統計資料  
</dl>

## <a name="setting-pgm-socket-options"></a>設定 PGM 通訊端選項

下列程式碼片段說明設定 PGM 通訊端選項的程式設計指導方針：


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



在上述程式碼片段中， *OptionData* 的類型和內容取決於所設定的通訊端選項。 針對所有的 PGM 通訊端選項，通訊端層級為 IPPROTO \_ RM。 您必須在呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函式之後立即設定 PGM 通訊端選項，但有下列例外狀況：

<dl> RM \_ 設定 \_ 訊息 \_ 界限  
RM 傳送者 \_ \_ 統計資料  
RM \_ 接收器 \_ 統計資料  
</dl>

 

 



