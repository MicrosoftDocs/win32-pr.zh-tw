---
description: 設定 [每個使用者的系統原則] 會指定安裝程式搜尋三種來源類型的順序。
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852931"
---
# <a name="searchorder"></a>SearchOrder

設定 [每個使用者的 [系統原則](system-policy.md) ] 會指定安裝程式搜尋三種來源類型的順序。 來源的類型為：

"n" –網路

"m" –媒體 (CD-ROM 或 DVD) 

"u" –統一資源定位器 (URL) 

例如，若要先搜尋網路來源、媒體來源第二個和 URL 來源，最後將此原則設定為 "nmu" 值。 若要省略搜尋特定來源類型，請從值中省略對應的字母。

如果未設定 SearchOrder，則預設搜尋順序為 [網路]、[媒體] 和 [URL]。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ SZ**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 



