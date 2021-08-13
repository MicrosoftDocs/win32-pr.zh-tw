---
description: 應用程式可以使用 RegSetValueEx 函式，將值和其資料與索引鍵建立關聯。 如需 RegSetValueEx 所支援之實數值型別的清單，請參閱登錄數值型別。
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: 寫入和刪除登錄資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd4e80dc3320d1af0931e111c82f473e0edf56ac071443397ffc3da0918f7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883990"
---
# <a name="writing-and-deleting-registry-data"></a>寫入和刪除登錄資料

應用程式可以使用 [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) 函式，將值和其資料與索引鍵建立關聯。 如需 **RegSetValueEx** 所支援之實數值型別的清單，請參閱登錄 [數值型別](registry-value-types.md)。

若要從索引鍵刪除值，應用程式可以使用 [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) 函數。 若要刪除索引鍵，可以使用 [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) 函數。 刪除的金鑰必須等到最後一個控制碼關閉後才會移除。 無法在已刪除的金鑰下建立子機碼和值。

您無法在寫入作業期間鎖定登錄機碼，以同步處理資料的存取。 不過，您可以使用安全性屬性來控制登錄機碼的存取。 如需詳細資訊，請參閱登錄機 [碼安全性和存取權限](registry-key-security-and-access-rights.md)。

您可以在單一交易內執行多個登錄作業。 若要建立登錄機碼與交易的關聯，應用程式可以使用 [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) 或 [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) 函數。 如需交易的詳細資訊，請參閱 [核心交易管理員](/windows/desktop/Ktm/kernel-transaction-manager-portal)。

 

 
