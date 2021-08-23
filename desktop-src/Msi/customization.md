---
description: 由於 Windows Installer 會保留關係資料庫中安裝的所有資訊，因此可以藉由將轉換作業套用至封裝，針對特定使用者群組自訂應用程式或產品的安裝。
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: 自訂
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ece84afd2b9ca5ce547d9ea96aed23786f78c89f01f5b5b5eaa78e2791e86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947852"
---
# <a name="customization"></a>自訂

由於 Windows Installer 會保留關係資料庫中安裝的所有資訊，因此可以藉由將轉換作業套用至封裝，針對特定使用者群組自訂應用程式或產品的安裝。 轉換可以用來封裝不同工作組所需之基底套件的各種自訂。 如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。

在安裝期間，可以即時套用多個基底套件的轉換。 這提供了一種機制，可有效率地將自訂安裝指派給不同的使用者群組。 例如，這在支援部門的公司需要不同的特定產品安裝時，才會很有用。 此產品可供組織中的所有人使用，方法是將基本套件的 [系統管理安裝](administrative-installation.md) 到單一系統管理安裝點。 然後每個工作群組都可以透過在安裝產品時的即時轉換，自動接收適當的自訂。

 

 



