---
description: 開發人員可以藉由開發 WMI 提供者來擴充 WMI 基礎結構。
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: 建立 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027561"
---
# <a name="creating-wmi-providers"></a>建立 WMI 提供者

開發人員可以藉由開發 WMI 提供者來擴充 WMI 基礎結構。 WMI 提供者是 COM 物件，可執行一組指定的介面，直到最近，一直都是在 c + + 中執行。 您現在可以使用 c # 之類的 managed 語言來執行 WMI 提供者。 3.5 版的 .NET framework 引進了 WMI 提供者延伸架構，讓這項功能得以實現。 若要深入瞭解如何使用該架構來建立 WMI 提供者，請參閱文章， [使用 WMI.NET 提供者延伸模組2.0 撰寫結合的 wmi 提供者](/previous-versions/dotnet/articles/cc268228(v=msdn.10))。

> [!Note]  
> 您也可以使用 Windows 管理基礎結構 (MI) （WMI 的下一代版本）來建立提供者。 如需詳細資訊，請參閱 [如何執行 MI 提供者](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider)。

 

下表說明本節中的內容。



| 主題                                                      | 描述                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [將資料提供給 WMI](providing-data-to-wmi.md)         | 概要說明建立 WMI 提供者所需的步驟。         |
| [開發 WMI 提供者](developing-a-wmi-provider.md) | 描述當您建立各種類型的 WMI 提供者時，必須執行的工作。 |



 

 

 
