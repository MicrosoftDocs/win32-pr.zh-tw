---
description: Unimodem 或通用數據機驅動程式 (Unimdm，) 提供幾乎所有標準數據機的存取權。
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4562ad7692c288a963db27b6859fa5c472d8ff80017e2726c277fbf9d24452be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011898"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

Unimodem 或通用數據機驅動程式 (Unimdm，) 提供幾乎所有標準數據機的存取權。 它支援允許半雙工串流的語音訊息。 Wave MSP 和 stream control 都有支援。  (請注意 Windows NT 4.0 或更早版本上的 Unimodem 不支援語音訊息，因此不可能進行直接串流控制。 ) 

此 TSP 支援 LINEADDRESSTYPE PHONENUMBER 的 [**網址類別型**](./lineaddresstype--constants.md) 值 \_ 。 如果程式設計人員想要使用撥號規則，則必須使用 TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) 介面或 Tapi 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) 功能，從標準格式的電話號碼取得可撥出的字串。

Unimodem TSP 會隨 Windows Server 2003 作業系統、Windows XP、Windows 2000、Windows NT、Windows Millennium Edition、Windows 98 和 Windows 95 一起安裝。

 

 
