---
description: 要變更系統狀態的自訂動作必須是延後執行自訂動作。
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: 使用自訂動作變更系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3ec2fafdc6f57041c087903da0c912327c967b3b188127ee1f2ff71db7c1af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086238"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>使用自訂動作變更系統狀態

要變更系統狀態的自訂動作必須是延後執行自訂動作。 藉由將資料列插入至順序資料表來設定屬性、功能狀態、元件狀態或目標目錄或排程系統作業的自訂動作，可以安全地使用立即執行。 不過，直接變更系統或呼叫另一個系統服務的自訂動作，必須延後至執行安裝腳本的時間。 如需詳細資訊，請參閱 [延後執行自訂動作](deferred-execution-custom-actions.md)。

您不應該嘗試使用立即執行自訂動作來變更系統狀態，因為每個變更狀態的自訂動作都必須有對應的復原自訂動作，才能在安裝復原時復原系統狀態變更。 所有的復原自訂動作也都是延後的自訂動作，而且必須在其復原的動作之前。 如需詳細資訊，請參閱 [復原自訂動作](rollback-custom-actions.md)。

 

 



