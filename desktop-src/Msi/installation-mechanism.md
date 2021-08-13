---
description: 成功的安裝程式有兩個階段：取得和執行。 如果安裝失敗，可能會發生復原階段。
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: 安裝機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bce4396701ab5cddb43a67dddbafd1e8310092d04d779af04ad7876681cc3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634216"
---
# <a name="installation-mechanism"></a>安裝機制

成功的安裝程式有兩個階段：取得和執行。 如果安裝失敗，可能會發生復原階段。

## <a name="acquisition"></a>擷取

在取得階段開始時，應用程式或使用者會指示安裝程式安裝功能或應用程式。 然後，安裝程式會執行安裝資料庫之順序資料表中所指定的動作。 這些動作會查詢安裝資料庫，並產生腳本，以提供執行安裝的逐步程式。

## <a name="execution"></a>執行

在執行階段中，安裝程式會將資訊以較高的許可權傳遞給處理常式，並執行腳本。

## <a name="rollback"></a>復原

如果安裝失敗，安裝程式會還原電腦的原始狀態。 當安裝程式處理安裝腳本時，它會同時產生 rollback 腳本。 除了 rollback 腳本，安裝程式還會在安裝期間儲存其所刪除之每個檔案的複本。 這些檔案會保存在隱藏的系統目錄中。 安裝完成之後，就會刪除復原腳本和儲存的檔案。 如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。

 

 



