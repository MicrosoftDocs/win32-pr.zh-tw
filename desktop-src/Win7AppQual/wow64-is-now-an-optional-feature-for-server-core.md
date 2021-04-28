---
description: WoW64 現在是 Server Core 的選擇性功能
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Server Core 中的 WoW64 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084046"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 現在是 Server Core 的選擇性功能

## <a name="affected-platforms"></a>受影響的平臺

**伺服器** -Windows Server 2008 R2  



## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

適用于 Windows Server 2008 R2 的 Server Core 安裝選項可讓您卸載 WoW64。 WoW64 現在是選擇性功能，如果不需要執行32位的程式碼，您可以將其卸載。

此外，Active Directory 和 Active Directory 輕量型目錄服務角色都需要 WoW64，才能在 Windows Server 2008 R2 中執行。

## <a name="manifestation-of-impact"></a>影響的表現

如果您卸載 WoW64，在 Server Core 上執行32位程式碼的系統管理員將會收到錯誤訊息，指出無法執行應用程式。 如果系統管理員嘗試執行 Active Directory 並 Active Directory 輕量型目錄服務，則會收到錯誤訊息。

## <a name="mitigation"></a>降低

安裝 WoW64。

## <a name="solution"></a>解決方法

慣用的解決方案是提供64位版本的程式碼，讓它可以在 Server Core 上執行，而不需要 WoW64。

至少，請提供使用者檔，請注意，若要執行32位程式碼，他們必須安裝 WoW64。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

確認所有使用的程式碼都是64位。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [WOW64 執行詳細資料](../winprog64/wow64-implementation-details.md)
-   [調試 WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
