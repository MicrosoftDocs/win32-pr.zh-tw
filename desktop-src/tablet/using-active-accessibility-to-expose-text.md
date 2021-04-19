---
description: 使用主動存取範圍來公開文字的總覽。
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: 使用 Active Accessibility 來公開文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973633"
---
# <a name="using-active-accessibility-to-expose-text"></a>使用 Active Accessibility 來公開文字

應用程式可以使用 Microsoft Active Accessibility 來公開文字。 不過，舊版 Active Accessibility 所定義的 [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) 介面未針對公開大量 rtf 文字進行優化。 較新的版本會定義已針對公開大量文字和文字屬性優化的介面。

若要公開大量文字，請建立個別的元件物件模型 (COM) 物件，這些物件支援 [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)或子項目，以代表每個文字執行。 執行是共用相同格式的一行或一行部分。

Active Accessibility 只會公開文字及其位置，但沒有公開文字格式的機制。 儘管有這些限制，某些程式還是會使用 Active Accessibility 來公開文字。 例如，Microsoft Internet Explorer 和 Microsoft Visual Studio 都會使用 Active Accessibility 來公開大量的文字。

如需使用 Active Accessibility 公開文字的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。

 

 
