---
description: 系統登錄提供者會嘗試針對每個發生的事件傳送一個通知。
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: 接收登錄事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f3c8f39be30beeb64e7c8d8ff7f1bacfba8a47b7f4bd0c70e7cf638bf726e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817454"
---
# <a name="receiving-registry-events"></a>接收登錄事件

系統登錄提供者會嘗試針對每個發生的事件傳送一個通知。 不過，系統登錄提供者不保證取用者會收到任何或所有事件。 例外狀況是系統登錄提供者會確保取用者每個事件註冊都會收到一個通知。

例如，假設取用者註冊了兩個樹狀變更事件，要求 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 實例的通知。 每個註冊都有相同的 Hive (子樹) 值，但有不同的 RootPath 值。 如果這兩個路徑中的金鑰多次變更，系統登錄提供者會保證取用者會收到每個路徑的通知。 視登錄和系統登錄提供者的回應時間而定，取用者可能會收到與事件發生次數一樣多的通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊系統登錄事件](registering-for-system-registry-events.md)
</dt> </dl>

 

 
