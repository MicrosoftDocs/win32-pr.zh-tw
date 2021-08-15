---
description: 最初必須建立安裝程式物件，以載入透過 COM 存取安裝程式元件所需的自動化支援。
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: 關於 Automation 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382065"
---
# <a name="about-the-automation-interface"></a>關於 Automation 介面

最初必須建立 [**安裝程式物件**](installer-object.md) ，以載入透過 COM 存取安裝程式元件所需的自動化支援。 這個物件會提供包裝函式來建立最上層的物件，並存取其方法。 這些包裝函式只會提供參數轉譯，以與 Microsoft Visual Basic 一致的方式公開安裝程式功能，而不會變更方法的行為。

可能的話，會將一組 Get 和 Set c + + 方法公開給 Visual Basic，以做為單一屬性。 在某些情況下，採用索引引數的 c + + 方法會公開為索引屬性。 許多 c + + 方法會透過參數傳回結果，因為傳回值是用於錯誤傳回。 不過，在 Visual Basic 中，錯誤是由個別的機制處理，而結果一律會傳入傳回值。

如需使用 automation 和建立安裝程式物件的詳細資訊，請參閱 [使用 Automation 介面](using-the-automation-interface.md)。

如需 Windows Installer 物件的參考資料，請參閱[Automation 介面參考](automation-interface-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



