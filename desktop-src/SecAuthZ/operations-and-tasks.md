---
description: 操作是低層級的電腦動作。
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: 作業和工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996836"
---
# <a name="operations-and-tasks"></a>作業和工作

操作是低層級的電腦動作。 在授權管理員 API 中，作業是由 [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) 物件表示。 一般情況下，作業數目太多，而且太低層級以促進系統管理。 將作業分組至工作中，以簡化授權原則的管理。

工作是以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件來代表，而且可以包含一或多個 [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) 物件。 **IAzTask** 物件也可以包含其他 **IAzTask** 物件，讓工作可以進行嵌套。 為了方便管理， **IAzTask** 物件應該代表實際使用者想要執行的工作。

與代表該工作的 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件相關聯的商務規則腳本，可以在執行時間限定對工作所包含之作業的存取權。 如需商務規則腳本的詳細資訊，請參閱 [商務規則](business-rules.md)。

[**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件也可以藉由將其 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition)屬性設定為 **TRUE** 來代表角色定義。 許可證 **管理員** MMC 嵌入式管理單元使用者介面會將該 **IAzTask** 物件顯示為角色。 如需角色定義的詳細資訊，請參閱 [角色](roles.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 c + + 中定義作業](defining-operations-in-c--.md)
</dt> <dt>

[在 c + + 中將作業分組為工作](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[在 c + + 中將工作分組為角色](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[使用者和群組](users-and-groups.md)
</dt> </dl>

 

 



