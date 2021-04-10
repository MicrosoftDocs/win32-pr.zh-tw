---
description: 內嵌的轉換會儲存在封裝的 .msi 檔案中。 這可保證使用者在安裝套件可用時，一律可使用轉換。 或者，您可以將轉換提供給使用者作為獨立的 .mst 檔案。
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: 內嵌轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026878"
---
# <a name="embedded-transforms"></a>內嵌轉換

內嵌的轉換會儲存在封裝的 .msi 檔案中。 這可保證使用者在安裝套件可用時，一律可使用轉換。 或者，您可以將轉換提供給使用者作為獨立的 .mst 檔案。

若要將內嵌轉換新增至轉換清單中，請在檔案名中加入冒號 (： ) 前置詞。 因為安裝程式一律會從 .msi 檔案中的儲存體取得轉換，所以不會在使用者的電腦上快取內嵌的轉換。 內嵌的轉換可搭配 [安全的轉換](secured-transforms.md) 或不 [安全的轉換](unsecured-transforms.md)一起使用。 如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。

 

 



