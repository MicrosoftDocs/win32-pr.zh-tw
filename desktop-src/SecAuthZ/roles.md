---
description: 角色在授權管理員中提供兩種不同的用途。
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: 角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848241"
---
# <a name="roles"></a>角色

角色在授權管理員中提供兩種不同的用途。 角色是使用者類別需要存取的一組工作或作業，而且也是一組符合該類別的使用者和群組。

-   [角色做為工作集](#roles-as-sets-of-tasks)
-   [角色做為使用者和群組的集合](#roles-as-sets-of-users-and-groups)
-   [相關主題](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>角色做為工作集

授權原則會將 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件，以建立一組工作。 所有指派給該 **IAzRole** 物件的使用者和群組，都具有存取這些 **IAzTask** 物件所包含之所有作業的許可權。

因為 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件代表一組工作，以及一組可存取這些工作的使用者和群組，所以授權管理員會提供一種方式來建立可指派給多個 **IAzRole** 物件的角色定義。 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件可以包含其他 **IAzTask** 物件。 然後，您可以將該 **IAzTask** 物件指派給一或多個 **IAzRole** 物件，以作為角色定義。 將 **IAzTask** 物件的 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition)屬性設定為 **TRUE** ，讓許可證 **管理員** MMC 嵌入式管理單元使用者介面將 **IAzTask** 物件顯示為角色。

## <a name="roles-as-sets-of-users-and-groups"></a>角色做為使用者和群組的集合

將使用者和群組指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole)物件，藉由呼叫 [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember)或 [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername)方法，將指派給該 **IAzRole** 物件之工作的存取權授與這些使用者和群組。 藉由呼叫 [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember)方法，將 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件所代表的現有應用程式群組指派給 **IAzRole** 物件。 指派給 **IAzRole** 物件的所有使用者和群組都可存取指派給該角色的工作和作業。 如需應用程式群組的詳細資訊，請參閱 [使用者和群組](users-and-groups.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 c + + 中將工作分組為角色](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[在 c + + 中定義使用者群組](defining-groups-of-users-in-c--.md)
</dt> <dt>

[在 c + + 中將使用者新增至應用程式群組](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



