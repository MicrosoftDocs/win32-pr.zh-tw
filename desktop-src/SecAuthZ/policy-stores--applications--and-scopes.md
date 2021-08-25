---
description: 授權原則存放區、應用程式和範圍代表授權管理員原則的不同層級。
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: 原則存放區、應用程式和範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db06b291ef81f391fed1a0094b73c9b31d0342f59bce22d93779c7bfa48a80b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907568"
---
# <a name="policy-stores-applications-and-scopes"></a>原則存放區、應用程式和範圍

授權原則存放區、應用程式和範圍代表授權管理員原則的不同層級。 原則存放區可包含一或多個應用程式，且應用程式可以包含一或多個範圍。

-   [授權原則存放區](#authorization-policy-stores)
-   [應用程式](#policy-stores-applications-and-scopes)
-   [範圍](#policy-stores-applications-and-scopes)
-   [委派](#delegation)
-   [相關主題](#related-topics)

## <a name="authorization-policy-stores"></a>授權原則存放區

在授權管理員 API 中，授權原則存放區會以 [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) 物件表示。 授權原則存放區包含應用程式、範圍、作業、工作、角色和使用者群組的定義和指派。

授權原則存放區可以儲存為 XML 檔案，或儲存在 Active Directory 中。

應用程式必須先初始化授權原則存放區，才能變更存放區中的資訊，或使用存放區原則來檢查用戶端對資源的存取。

授權原則存放區可以包含一或多個 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，每個物件都代表特定應用程式的授權原則。

## <a name="applications"></a>應用程式

在授權管理員 API 中，應用程式是以 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件表示。 授權原則存放區可包含許多應用程式的授權原則資訊。 使用 **IAzApplication** 物件可讓您將不同應用程式的不同授權原則儲存在單一原則存放區中。

一個授權原則存放至少必須包含一個應用程式。

## <a name="scopes"></a>範圍

在授權管理員 API 中，範圍是由 [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) 物件表示。 範圍為授權原則提供額外的選擇性組織層級。 應用程式可包含一或多個範圍，但不需要包含任何 (授權管理員提供預設的全應用程式範圍) 。

範圍是應用程式內的細分，可將資源與該應用程式所使用的其他資源分隔開來。 若有不想將其套用於整個應用程式的授權管理員群組、角色指派、角色定義或工作定義，請將它們建立為領域層級。

## <a name="delegation"></a>委派

儲存在 Active Directory 支援管理委派的授權原則存放區。 系統管理可以委派給存放區、應用程式或範圍層級的使用者和群組。 每個層級都會定義該層級之原則的系統管理角色。 若要將控制項委派給使用者或群組，請將控制權指派給系統管理員角色。若要允許使用者或群組讀取原則，請將其指派給 [讀者] 角色。

存放區、應用程式或範圍的系統管理員可以讀取和修改委派層級的原則存放區。 讀取器可以讀取委派層級的原則存放區，但無法修改存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 c + + 中建立授權原則存放區物件](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[在 c + + 中建立應用程式物件](creating-an-application-object-in-c--.md)
</dt> <dt>

[委派 c + + 中的許可權定義](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



