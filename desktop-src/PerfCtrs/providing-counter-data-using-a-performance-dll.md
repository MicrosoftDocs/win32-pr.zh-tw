---
description: 需要提供計數器資料的服務、驅動程式或應用程式可以撰寫效能 DLL 來提供資料。
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: 使用效能 DLL 提供計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 165e6a8797c50a22acff1d3cd3ded7f8b06a0ee2a7153300e98e46bea1127f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910308"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>使用效能 DLL 提供計數器資料

> [!IMPORTANT]
> 由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。

需要提供計數器資料的服務、驅動程式或應用程式可以撰寫效能 DLL 來提供資料。 當取用者查詢效能資料時，系統會將提供者 DLL 載入取用者的進程，並呼叫提供者來收集資料。 如需撰寫效能 DLL 的詳細資訊，請參閱 [建立效能延伸模組 dll](creating-a-performance-extension-dll.md)。

系統會使用登錄來判斷要呼叫的提供者。 如需註冊提供者及其支援之計數器的詳細資訊，請參閱 [新增效能計數器](adding-performance-counters.md)。

> [!Note]
> Windows OneCore 不支援效能 Dll。 如果要撰寫必須在 Windows OneCore 上執行的元件，請使用在[使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)中所述的方法。
