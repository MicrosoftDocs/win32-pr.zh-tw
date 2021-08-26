---
description: 設定 [每個使用者的系統原則] 會指定安裝程式搜尋三種來源類型的順序。
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041038"
---
# <a name="searchorder"></a>SearchOrder

設定 [每個使用者的 [系統原則](system-policy.md) ] 會指定安裝程式搜尋三種來源類型的順序。 來源的類型為：

"n" –網路

"m" –媒體 (CD-ROM 或 DVD) 

"u" –統一資源定位器 (URL) 

例如，若要先搜尋網路來源、媒體來源第二個和 URL 來源，最後將此原則設定為 "nmu" 值。 若要省略搜尋特定來源類型，請從值中省略對應的字母。

如果未設定 SearchOrder，則預設搜尋順序為 [網路]、[媒體] 和 [URL]。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_\_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **安裝程式** 的目前使用者軟體原則

## <a name="data-type"></a>資料類型

**REG \_ SZ**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 



