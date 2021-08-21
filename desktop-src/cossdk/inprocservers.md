---
description: 包含向系統註冊的同進程伺服器清單。 它包含每個元件的物件，該物件會註冊為同進程伺服器。
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: InprocServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: b751f007082454832fe31172e35b834b66c36d13dbaf6a6687ba0036879b60c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047456"
---
# <a name="inprocservers-collection"></a>InprocServers 集合

包含向系統註冊的同進程伺服器清單。 它包含每個元件的物件，該物件會註冊為同進程伺服器。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。 若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。

## <a name="members"></a>成員

**InprocServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 元件的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                  |
| 類型           | String                                                                                                                                                    |
| 預設值        | N/A                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>InprocServer32



| 進入 | 值 |
|----------------|----------------------------------|
| 描述    | 元件的檔案路徑。 |
| Access         | ReadOnly                         |
| 類型           | String                           |
| 預設值        | N/A                              |
| 最小系統 | Windows 2000                     |



 

### <a name="progid"></a>ProgID



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 識別元件的名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                            |
| 類型           | String                                                                                                                                                              |
| 預設值        | N/A                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
