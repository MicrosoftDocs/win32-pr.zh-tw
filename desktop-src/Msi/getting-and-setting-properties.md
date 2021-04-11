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
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="ae308-103">取得和設定屬性 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="ae308-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="ae308-104">若要在安裝中使用 [屬性](properties.md) ，您可以使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 和 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) 來取得和設定程式的屬性值，並將它包含在安裝資料庫中做為條件陳述式的一部分。</span><span class="sxs-lookup"><span data-stu-id="ae308-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="ae308-105">若要取得目前的屬性，請呼叫 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae308-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="ae308-106">若要取得目前的安裝狀態，請呼叫 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae308-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="ae308-107">若要取得目前安裝的語言，請呼叫 [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae308-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="ae308-108">若要設定屬性，請呼叫 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae308-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="ae308-109">若要設定安裝狀態，請呼叫 [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae308-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="ae308-110">若要清除屬性 (將它設定為 Null) ，請將屬性的值設為空字串： ""。</span><span class="sxs-lookup"><span data-stu-id="ae308-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae308-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae308-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae308-112">使用屬性</span><span class="sxs-lookup"><span data-stu-id="ae308-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="ae308-113">在命令列上設定公用屬性值</span><span class="sxs-lookup"><span data-stu-id="ae308-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="ae308-114">清除安裝程式屬性</span><span class="sxs-lookup"><span data-stu-id="ae308-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 



