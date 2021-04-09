---
description: 包含應用程式叢集中的伺服器電腦清單。 它包含每一部伺服器的物件。
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: ApplicationCluster 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110565"
---
# <a name="applicationcluster-collection"></a>ApplicationCluster 集合

包含應用程式叢集中的伺服器電腦清單。 它包含每一部伺服器的物件。 這是最上層集合。

應用程式叢集是針對 (CLB) 服務的元件負載平衡而定義的。 針對要使用的應用程式叢集集合，必須在電腦上安裝 CLB 服務。

您可以使用 [**LocalComputer**](localcomputer.md) 集合物件上的 IsRouter 屬性，指定應用程式叢集中的路由器，然後指定指定的元件應該與 [**元件**](components.md) 集合物件上的 LoadBalancingSupported 屬性進行負載平衡。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**ApplicationCluster** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [名稱](#name)

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 伺服器的名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                            |
| 類型           | String                                                                                                                                                                                                                                                               |
| 預設值        | 「新增電腦」                                                                                                                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
