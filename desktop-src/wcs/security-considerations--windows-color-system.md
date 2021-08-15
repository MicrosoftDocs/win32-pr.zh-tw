---
title: Windows 色彩系統的安全性考慮
description: Windows 色彩系統的安全性考慮
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- WindowsColor System (WCS) ，安全性
- WCS (Windows 色彩系統) ，安全性
- 影像色彩管理，安全性
- 色彩管理，安全性
- Windows 色彩系統 (WCS) 的安全性
- '色彩管理模組 (CMM) '
- " (色彩管理模組) 的 CMM"
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444665"
---
# <a name="security-considerations-windows-color-system"></a>安全性考慮： Windows 色彩系統

本檔提供與影像色彩管理相關之安全性考慮的資訊。 本檔並不提供您需要瞭解的安全性問題，而是使用它作為此技術領域的起點和參考。

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>非 Microsoft Cmm 可以在系統內容中執行

非 Microsoft 色彩管理模組 (Cmm) 應該視為非 Microsoft 印表機驅動程式，因為它們有可能在系統內容中執行，以進行列印工作。
