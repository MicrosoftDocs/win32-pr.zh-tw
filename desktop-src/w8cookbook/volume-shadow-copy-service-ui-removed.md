---
title: 已移除本機磁片區的舊版 UI
description: 已移除本機磁片區的舊版 UI
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463829"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>已移除本機磁片區的舊版 UI

## <a name="platform"></a>平台

**用戶端** – Windows 8 


## <a name="description"></a>Description

舊版 Windows 允許使用者從本機磁片區的「陰影複製」還原舊版的個別檔案。 這些陰影複製是透過磁片區陰影複製服務 (VSS) ，由「先前的版本」功能所建立。 在 Windows 7 中，使用者可以在系統屬性提供的系統保護 UI 中，設定和排程陰影複製。

不過，先前的版本很少使用，且會對整體 Windows 效能造成負面影響;因此已移除此功能。 在 Windows 8 中，這些功能已無法再使用：

-   可以透過舊版 UI 流覽、搜尋或還原先前版本的檔案
-   透過系統保護 UI 設定或排程先前版本檔案的能力

不過，使用者在存取 Windows server 上的檔案共用時，仍可使用 [先前的版本] 索引標籤。

## <a name="manifestation"></a>表現

在 [Windows 檔案總管內容] 功能表中，本機磁片區無法再使用 [先前的版本] 選項。

## <a name="solution"></a>解決方法

需要建立本機磁片區陰影複製的開發人員仍然可以藉由呼叫自訂程式碼中的 VSS Api 來這麼做。

 

 




