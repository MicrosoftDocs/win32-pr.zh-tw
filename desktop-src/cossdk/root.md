---
description: 包含目錄中的最上層集合。
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: 根集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0aba7a308a37ee531adf0886b8d06d4fd8c17369f73bd2bddf3211c2c184a4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547015"
---
# <a name="root-collection"></a>根集合

包含目錄中的最上層集合。 它不包含任何 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件或支援任何屬性。

**根** 集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

您無法從任何集合流覽至 **根** 集合。

## <a name="members"></a>成員

**根** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

以下是目錄中的最上層集合：

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**應用程式**](applications.md)
-   [**ComputerList**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServers**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**分割區**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
