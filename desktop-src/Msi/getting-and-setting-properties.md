---
description: 若要在安裝中使用屬性，您可以使用 MsiGetProperty 和 MsiSetProperty 來取得和設定程式的屬性值，並將它包含在安裝資料庫中做為條件陳述式的一部分。
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: '取得和設定屬性 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850212"
---
# <a name="getting-and-setting-properties-windows-installer"></a>取得和設定屬性 (Windows Installer) 

若要在安裝中使用 [屬性](properties.md) ，您可以使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 和 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) 來取得和設定程式的屬性值，並將它包含在安裝資料庫中做為條件陳述式的一部分。

-   若要取得目前的屬性，請呼叫 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 函數。
-   若要取得目前的安裝狀態，請呼叫 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 函數。
-   若要取得目前安裝的語言，請呼叫 [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) 函數。
-   若要設定屬性，請呼叫 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) 函數。
-   若要設定安裝狀態，請呼叫 [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) 函數。
-   若要清除屬性 (將它設定為 Null) ，請將屬性的值設為空字串： ""。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用屬性](using-properties.md)
</dt> <dt>

[在命令列上設定公用屬性值](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[清除安裝程式屬性](clearing-an-installer-property.md)
</dt> </dl>

 

 



