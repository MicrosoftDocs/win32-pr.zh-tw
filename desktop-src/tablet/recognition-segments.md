---
description: 辨識區段是辨識器在內部用來產生特定筆墨物件之辨識結果的基本筆墨單位。
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: 辨識區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997944"
---
# <a name="recognition-segments"></a>辨識區段

辨識區段是辨識器在內部用來產生特定筆墨物件之辨識結果的基本筆墨單位。 辨識區段是筆墨筆劃的集合。 例如，辨識器能夠辨識英文的手寫手寫，可能會使用單字作為基本辨識區段。

其他辨識器可能會使用複合單字的一部分作為基本區段。 例如，在西班牙文中，簡短的單字通常會結合以提供較長的複合字組。 "Damelo" 是由三個字組 "da me lo" 組成的西班牙文， (給我) ，但它是以單一單字寫成。 西班牙文辨識器可以將每個部分字組辨識為區段。

辨識器可能會發現數種將筆墨範例分成辨識區段的方式。 由於辨識使用者的預期輸入需要混淆，因此辨識器可能會傳回許多替代相符專案。

如需替代項的詳細資訊，請參閱 [替代](alternates.md)。

 

 



