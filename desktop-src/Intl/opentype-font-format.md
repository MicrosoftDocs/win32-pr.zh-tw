---
description: 以 Unicode 為基礎的 OpenType 字型格式可延伸 TrueType 字型檔案格式。
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: OpenType 字型格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988457"
---
# <a name="opentype-font-format"></a>OpenType 字型格式

以 Unicode 為基礎的 OpenType 字型格式可延伸 TrueType 字型檔案格式。 OpenType [字型](uniscribe-glossary.md)允許在字元和字元之間進行對應，以支援連字號、位置形式、替代項和其他替代。 OpenType 字型也可以包含支援二維圖像定位和圖像附件的資訊，而且可以包含 TrueType 或 PostScript 大綱。

OpenType 字型內的版面配置功能是依腳本和語言來組織，允許單一字型支援多個書寫系統，即使在同一個腳本內也一樣。 為了確保文字版面配置作業的一致性，並避免字型檔案或應用程式中不必要的額外負荷，Uniscribe 中包含許多文字配置和語言語義演算法。 如此一來，字型開發人員就不需要在字型內定義一般化腳本規則。

應用程式可能會引入有關腳本配置的特定知識或喜好設定。 OpenType 版面配置字型甚至可能包含複製或取代作業系統服務所套用的配置規則。 支援文字配置之作業系統服務的分層結構，可讓應用程式選擇要使用的配置資訊，然後選取要套用的版面配置資訊。 如需詳細資訊，請參閱 [Microsoft 印刷樣式規格總覽](https://www.microsoft.com/typography/SpecificationsOverview.mspx) 或 [OpenType 規格](https://www.microsoft.com/typography/otspec/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



