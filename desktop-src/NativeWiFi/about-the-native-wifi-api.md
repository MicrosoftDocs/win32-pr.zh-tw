---
description: 原生 Wifi API 包含支援無線網路連線能力和無線設定檔管理的功能、結構和列舉。
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: 關於原生 Wifi API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194942"
---
# <a name="about-the-native-wifi-api"></a>關於原生 Wifi API

原生 Wifi API 包含支援無線網路連線能力和無線設定檔管理的功能、結構和列舉。 API 可用於基礎結構和臨機操作網路。 無線臨機操作 API 是簡化的物件導向介面，用來建立、管理和使用臨機操作網路。

> [!Note]  
> 未來的 Windows 版本可能無法使用臨機操作模式。 從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 [Wi-Fi Direct](about-the-wi-fi-direct-api.md) 。

 

特定 API 的執行會使用原生 Wifi API。 這表示臨機操作 API 呼叫可以觸發原生 Wifi 通知，反之亦然。

不建議混合原生 Wifi API 呼叫和無線臨機操作 API 呼叫。 開發人員應該在設計應用程式之前，先選擇程式設計方法。 如果您的應用程式使用或管理基礎結構網路，您應該使用原生 Wifi API。 如果您的應用程式需要設定檔管理功能，您應該使用原生 Wifi API。 否則，您應該使用無線特定 API。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於原生 Wifi](about-native-wifi.md)
</dt> <dt>

[Windows XP 上的原生 Wifi API 支援](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[原生 Wifi API 許可權](native-wifi-api-permissions.md)
</dt> <dt>

[關於無線特定 API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[下載 Windows Vista SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



