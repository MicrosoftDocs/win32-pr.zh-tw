---
title: ADSI WinNT 提供者
description: Microsoft ADSI 提供者會執行一組 ADSI 物件來支援各種 ADSI 介面。
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- adsi winnt 提供者 ADSI
- WinNT 服務提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371847"
---
# <a name="adsi-winnt-provider"></a>ADSI WinNT 提供者

Microsoft ADSI 提供者會執行一組 ADSI 物件來支援各種 ADSI 介面。 Windows 提供者的命名空間名稱是「WinNT」，而這個提供者通常稱為 WinNT 提供者。 若要存取 WinNT 提供者，請使用[Winnt AdsPath](winnt-adspath.md)系結至 winnt 的任何[ADSI 物件](adsi-objects-of-winnt.md)。

WinNT 提供者包含在適用于 Windows 和 Windows Server 的 ADSI 系統元件中。

> [!Note]  
> 預設的 WinNT 提供者無法假設為完全安全線程。 多執行緒應用程式的寫入器應該會處理多執行緒處理，以適當地協調執行緒之間的任何存取，例如信號、mutex、重要區段等等。

 

 

 




