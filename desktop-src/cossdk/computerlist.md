---
description: 包含 [元件服務] 系統管理工具的 [電腦] 資料夾中的電腦清單。 它包含每一部電腦的物件。
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: ComputerList 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468197"
---
# <a name="computerlist-collection"></a>ComputerList 集合

包含 [元件服務] 系統管理工具的 [ **電腦** ] 資料夾中的電腦清單。 它包含每一部電腦的物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**ComputerList** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

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
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 電腦的名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                                                 |
| 預設值        | 「新增電腦」                                                                                                                                                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
