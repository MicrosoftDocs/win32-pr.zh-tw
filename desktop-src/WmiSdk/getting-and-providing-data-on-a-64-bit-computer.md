---
description: 存取標準 WMI 32 位提供者的用戶端應用程式和腳本在64位作業系統上執行時，會繼續正常運作。
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: 在64位電腦上取得和提供資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819374"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>在64位電腦上取得和提供資料

存取標準 WMI 32 位提供者的用戶端應用程式和腳本在64位作業系統上執行時，會繼續正常運作。 只有兩個預先安裝的提供者（ [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 和 [View provider](view-provider.md)）具有與32位版本並存執行的64位版本。 不過，要求32位 Windows Driver Model (WDM) 實例的32位應用程式會收到64位作業系統上的預設64位 WDM 類別實例。

## <a name="accessing-default-and-nondefault-provider-data"></a>存取預設和非預設的提供者資料

一般而言，提供者寫入器不會同時在相同的作業系統中包含32位和64位版本的提供者。 如果沒有64位提供者存在，32位提供者可以繼續透過 WOW64 的功能執行。 64位提供者同樣可以提供資料給32位應用程式。 如需詳細資訊，請參閱 [在64位平臺上提供 WMI 資料](providing-wmi-data-on-a-64-bit-platform.md)。

如果有兩個版本，用戶端應用程式和腳本可以使用 [COM API](com-api-for-wmi.md) 和 [腳本 API](scripting-api-for-wmi.md) 中提供的內容參數，明確地連接到特定非預設的 WMI 提供者（如果有的話）。 如需詳細資訊，請參閱 [在64位平臺上要求 WMI 資料](requesting-wmi-data-on-a-64-bit-platform.md)。

下圖顯示預設和非預設的連線，使用登錄作為範例，讓兩個提供者可以並存于64位平臺上。

![64位平臺上的預設和非預設連接](images/32-64bit-registry.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在64位平臺上要求 WMI 資料](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[在64位平臺上提供 WMI 資料](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
