---
description: 瞭解 PrintCapabilities 架構所加諸的限制。 PrintCapabilities 提供者必須偵測到不正確設定，並加以解決。
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed 限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404921"
---
# <a name="schema-imposed-limitations"></a>Schema-Imposed 限制

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 架構提供 PrintCapabilities 作者大量的彈性和表達，可用於裝置描述。 不過，設定相依性對此彈性和表達有限制。 ParameterDef 實例、功能元素清單、每個功能內的選項實例清單，以及每個選項內的 ScoredProperty 實例都不得包含設定相依性。 PrintCapabilities 檔提供者必須偵測到不正確設定組合，而且必須加以解決。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



