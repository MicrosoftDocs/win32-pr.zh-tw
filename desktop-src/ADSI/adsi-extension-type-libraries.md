---
title: ADSI 擴充功能類型程式庫
description: 延伸模組的類型程式庫不會合並。
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI 擴充功能類型程式庫 ADSI
- 延伸模組 ADSI、延伸型別程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180828"
---
# <a name="adsi-extension-type-libraries"></a>ADSI 擴充功能類型程式庫

延伸模組的類型程式庫不會合並。 ADSI 用戶端必須特別包含每個延伸模組的類型程式庫。 Visual Basic 需要類型程式庫才能啟用早期繫結。 以 C/c + + 撰寫的用戶端應用程式可以在延伸模組標頭檔中定義的延伸模組介面上呼叫 **QueryInterface** 方法。

 

 




